# PHP | chmod()函数

> 原文:[https://www.geeksforgeeks.org/php-chmod-function/](https://www.geeksforgeeks.org/php-chmod-function/)

PHP 中的 chmod()函数是一个内置函数，用于将指定文件的模式更改为用户给定的特定模式。
chmod()函数改变指定文件的权限，成功返回 true，失败返回 false。

**语法:**

```php
bool chmod ( string $filename, int $mode )
```

**使用的参数:**
PHP 中的 chmod()函数接受两个参数，即文件名和模式。

1.  **$filename** :指定需要更改权限的文件。
2.  **$模式**:用于指定新权限。
    模式参数由四个数值组成，其中第一个值始终为零，第二个值指定所有者的权限，第三个值指定所有者用户组的权限，第四个值指定其他所有人的权限。
    有三个可能的值，要设置多个权限，可以添加以下值。
    *   1 =执行权限
    *   2 =写权限
    *   4 =读取权限

**返回值:**成功执行返回真，失败返回假。

**错误和异常**:

1.  PHP 中的 chmod()函数不适用于远程文件。它只对服务器文件系统可访问的文件起作用。
2.  如果在$mode 参数周围使用引号，例如 chmod (file.txt，“0744”)，那么 PHP 将隐式转换为整数数据类型。

示例:

```php
Input : chmod("gfg.txt", 0600);
Output : true

Input : chmod("gfg.txt", 0644);
Output : true

Input : chmod("gfg.txt", 0755);
Output : true
```

下面的程序说明了 PHP 中的 chmod()函数:

**程序 1** :

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Read and write permission to owner
chmod("gfg.txt", 0600);

?>
```

输出:

```php
true
```

**程序 2** :

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Read and write permission to owner,
// and read permission to everyone else
chmod("gfg.txt", 0644);

?>
```

输出:

```php
true
```

**程序 3** :

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// All permissions to owner, read and
// execute permissions to everyone else
chmod("gfg.txt", 0755);

?>
```

输出:

```php
true
```

**参考:**T2[http://php.net/manual/en/function.chmod.php](http://php.net/manual/en/function.chmod.php)T5】