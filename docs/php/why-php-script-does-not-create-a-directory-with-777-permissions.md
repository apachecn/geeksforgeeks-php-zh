# PHP 脚本为什么不创建一个 777 权限的目录？

> 原文:[https://www . geesforgeks . org/why-PHP-script-not-create-a-directory-with-777-permissions/](https://www.geeksforgeeks.org/why-php-script-does-not-create-a-directory-with-777-permissions/)

在 PHP 中，由于默认的 **umask** ，我们无法创建具有 777 权限的目录。 **umask** 被称为用户掩码或用户文件创建掩码。这是创建新文件或文件夹时给出的一种基本权限或默认权限。 **umask** 的默认值一般为 **022** 。 **umask** 设置在创建文件或目录时，必须从系统默认设置中删除哪些权限。

首先，让我们了解一下 **umask** 在文件或目录创建和权限设置过程中实际是如何工作的。我们将在下面的例子中使用 [mkdir()](https://www.geeksforgeeks.org/php-mkdir-function/)) 函数。

*   **例 1:**

```php
For example, a mask 0022 means that you don't want 
group and others modify the file.

default 0666 rw-.rw-.rw-
umask   0022 ---.-w-.-w-
Final   0644 rw-.r--.r--

That means any file from now will have 0644 permissions.
```

重要的是要理解 **umask** 撤销、删除系统默认的权限，所以它不能授予系统默认没有的权限。在上例中，在 666 系统默认情况下，您无法使用 **umask** 创建具有执行权限的文件。

*   **Example 2:** Suppose the permission of new directory created to be 665 OR mkdir(“geeks”, 655); The folder “geeks” will have permission: **drw–wx-wx** 

```php
The original permission according to 655 is drw-r-xr-x.
But the result is drw--wx-wx.
Permission to be applied: 655
Default umask           : 022
Final                   : 633

This is obtained by performing subtraction.
```

所以，当我们试图创建一个拥有权限 777 的目录时，我们得到的不是 **drwxrwxrwx** ，而是 **drwxr-xr-x** ，对应于 755(从 777 中减去 022)。这就是为什么我们无法创建具有权限 777 的目录的原因。

这还没有结束，因为我从来没有说过创建一个拥有权限 777 的目录是不可能的。那么我们来学习一下如何创建一个拥有 777 权限的目录，按照下面的步骤:

*   **步骤 1:** 该行将 **umask** 更改为零，同时将前一个存储到 **$oldmask** 中。

```php
$oldmask = umask(0)
```

*   **步骤 2:** 这一行使目录使用所需的权限和(现在不相关) **umask** 。

```php
mkdir("Geeks", 777);
```

*   **第三步:**这条线将 **umask** 恢复到原来的状态。

```php
umask($oldmask);
```

这就是如何创建一个拥有 777 权限的目录。目录符号表示的权限 **777** 是 **drwxrwxrwx** 。此权限允许所有者用户、组和其他人读取、写入和执行，因此没有限制。该权限意味着同一服务器上的任何用户都可以读取、写入和执行该文件。在文件夹的情况下，任何用户都可以将文件复制到其中。如果您的网站使用共享服务器，这显然听起来很危险。

**参考文献:**T2https://www.php.net/manual/en/function.umask.php