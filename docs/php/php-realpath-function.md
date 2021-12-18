# PHP|realpath()函数

> Original: [https://www.geeksforgeeks.org/php-realpath-function/](https://www.geeksforgeeks.org/php-realpath-function/)

PHP 中的 realpath()函数是一个内置函数，用于返回规范化的绝对路径名。
realpath()函数删除所有符号链接，如**‘/./’/../‘**和额外的**’/‘**，并返回绝对路径名。
路径作为参数发送给 realpath()函数，成功时返回绝对路径名，失败时返回 False。

**语法：**

```php
realpath(path)
```

**使用的参数：**
PHP 中的 realpath()函数只接受一个参数。

*   **path：**必选参数，指定用户想知道其绝对路径的符号路径。

**返回值：**
成功时返回绝对路径名，失败时返回 false。

**错误和异常**

1.  如果运行的脚本对层次结构中的所有目录都没有可执行权限，则 realpath()函数返回 False。
2.  函数 realpath()不适用于 Phar 中的文件，因为这样的路径不是真实路径。
3.  某些文件系统函数可能会为大于 2 GB 的文件返回意外结果，因为 PHP 的整数类型是 SIGNED 的，并且许多平台使用 32 位整数。

例如：

```php
Input : echo realpath("gfg.txt");
Output : C:\xampp\htdocs\filehandling\gfg.txt

Input : chdir('/docs/assignment/');
        echo realpath('./../../gfg/articles');

Output : /gfg/articles

```

下面的程序演示 realpath()函数。

假设有一个名为“gfg.txt”的文件

**程序 1**

```php
<?php 
// returning absolute path 
// using realpath() function
echo realpath("gfg.txt");

?>
```

发帖主题：Re：Колибри0.7.0

```php
C:\xampp\htdocs\filehandling\gfg.txt
```

**程序 2**

```php
<?php 

// using chdir() to change directory
chdir('/docs/assignment/');

// returning absolute path using realpath() function
echo realpath('./../../gfg/articles');

?>
```

发帖主题：Re：Колибри0.7.0

```php
/gfg/articles
```

**引用：**
[http://php.net/manual/en/function.realpath.php](http://php.net/manual/en/function.realpath.php)