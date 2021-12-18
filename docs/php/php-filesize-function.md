# PHP|filesize()函数

> Original: [https://www.geeksforgeeks.org/php-filesize-function/](https://www.geeksforgeeks.org/php-filesize-function/)

PHP 中的 filesize()函数是一个内置函数，用于返回指定文件的大小。 函数的作用是：接受文件名作为参数，成功时返回文件大小(以字节为单位)，失败时返回 FALSE。

将缓存 filesize()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```php
filesize($filename)
```

**参数：**PHP 中的 filesize()函数只接受一个参数*$filename*。 它指定要检查其大小的文件的文件名。

**返回值：**成功时返回文件大小，失败时返回 False。

**错误和异常**：

1.  对于大于 2 GB 的文件，某些文件系统函数可能会返回意外结果，因为 PHP 的整数类型是有符号的，并且许多平台使用 32 位整数。
2.  如果多次使用 filesize()函数，则必须清除缓冲区。
3.  函数的作用是：在出现故障时发出 E_WARNING。

**示例：**

```php

Input : echo filesize("gfg.txt");
Output : 256

Input : $myfile = 'gfg.txt';
        echo $myfile . ': ' . filesize($myfile) . ' bytes';
Output : gfg.txt : 256 bytes

```

下面的程序说明了 filesize()函数。

**程序 1**：

```php
<?php

// displaying file size using
// filesize() function
echo filesize("gfg.txt");

?>
```

产出：

```php
256
```

**程序 2**：

```php
<?php

// displaying file size using
// filesize() function
$myfile = 'gfg.txt';

echo $myfile . ': ' . filesize($myfile) . ' bytes';

?>
```

产出：

```php
gfg.txt : 256 bytes
```

**引用：**
[http://php.net/manual/en/function.filesize.php](http://php.net/manual/en/function.filesize.php)