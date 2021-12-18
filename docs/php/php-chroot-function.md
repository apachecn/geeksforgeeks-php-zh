# PHP | chroot()函数

> 原文:[https://www.geeksforgeeks.org/php-chroot-function/](https://www.geeksforgeeks.org/php-chroot-function/)

PHP 中的 chroot()函数是一个内置函数，用于将当前进程的根目录改为目录。函数的作用是:将当前工作目录修改为“/”。chroot()功能仅适用于 GNU 和 BSD 系统，并且仅在用户使用 CLI、CGI 或嵌入式 SAPI 时可用。除此之外，chroot()函数还需要 root 权限才能运行。

**语法:**

```php
chroot($directory)
```

**使用的参数:**PHP 中的 chroot()函数只接受一个参数，如下所述。

*   **$ directory** : This is a mandatory parameter that specifies the new path to which the root directory must be changed.

**返回值:**成功返回真，失败返回假。

**错误和异常**:

1.  chroot()函数在 windows 平台上尚不可用。
2.  除了 GNU 和 BSD 之外，chroot()函数也可以在 SVR4 平台上使用。

下面的程序说明了 chroot()函数:

**节目 1:**

```php
<?php

// Changing root directory
chroot("/path/gfg/chroot/");

// displaying current directory
echo getcwd();
?>
```

**输出:**

```php
/

```

**节目 2:**

```php
<?php
// Changing root directory
$flag = chroot("path/gfg/chroot/");
if($flag == true) 
{ 
   echo("Root Directory Has Been Successfully Changed");
} 
else 
{
   echo("Root Directory Cannot Be Changed");
} 
?>
```

**输出:**

```php
Root Directory Has Been Successfully Changed

```

**参考:**T2】http://php.net/manual/en/function.chroot.php