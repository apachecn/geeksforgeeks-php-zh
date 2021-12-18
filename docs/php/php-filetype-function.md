# PHP|filetype()函数

> Original: [https://www.geeksforgeeks.org/php-filetype-function/](https://www.geeksforgeeks.org/php-filetype-function/)

PHP 中的 filetype()函数是一个内置函数，用于返回指定文件或目录的文件类型。

函数的作用是：接受文件名作为参数，成功时返回七种文件类型之一，失败时返回 False。

Filetype()函数的七个可能返回值为：

*   文件：常规文件
*   目录：目录
*   CHAR：字符专用设备
*   链接：符号链接
*   FIFO：FIFO(命名管道)
*   BLOCK：BLOCK 特殊设备
*   未知：未知的文件类型

将缓存 filetype()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```php
filetype( $filename )
```

**参数：**PHP 中的 filetype()函数只接受一个参数*$filename*。 它指定您想要了解其类型的文件的文件名。

**返回值：**成功时返回文件类型，失败时返回 False。

**错误和异常**：

1.  对于大于 2 GB 的文件，某些文件系统函数可能会返回意外结果，因为 PHP 的整数类型是有符号的，并且许多平台使用 32 位整数。
2.  函数的作用是：在出现故障时发出 E_WARNING。
3.  如果多次使用 filetype()函数，则必须清除缓冲区。
4.  如果 stat 调用失败或文件类型未知，则 filetype()函数会发出一条 E_NOTICE 消息。

例如：

```php
Input : filetype("gfg.txt");
Output : file

Input : filetype("documents");
Output : dir

```

下面的程序演示了 filetype()函数。

**程序 1**：

```php
<?php

// displaying file type using
// filetype() function
echo filetype("gfg.txt");

?>
```

产出：

```php
file
```

**程序 2**：

```php
<?php

// displaying file type using
// filetype() function
$myfile = "documents";

echo $myfile . ': ' . filetype($myfile);

?>
```

产出：

```php
documents : dir
```

**引用：**
[http://php.net/manual/en/function.filetype.php](http://php.net/manual/en/function.filetype.php)