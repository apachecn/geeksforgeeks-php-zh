# PHP|SplFileObject Seek()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-seek-function/](https://www.geeksforgeeks.org/php-splfileobject-seek-function/)

**SplFileObject：：Seek()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于查找指定行。

**语法：**

```php
*void* SplFileObject::seek( $line_num)
```

**参数：**此函数只接受一个指定文件行号的参数$line_num。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 SplFileObject：：Seek()函数：

**程序-1：**

```php
<?php

// PHP program to illustrate
// SplFileObject Seek function

$file = new SplFileObject(__FILE__);

$file->seek(3);

echo $file->current();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序-2：**

```php
<?php 

// PHP program to use array to check 
// multiple files 
$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "gfg.txt",
    "mime.php"
    );

foreach ($GFG as &$file_name) { 

    $file = new SplFileObject($file_name);
    $file->seek(3);
    echo $file->current();
    }
?>
```

**输出：**

```php
GeeksforGeeks
gfg
contribute

```

**引用：**[http://php.net/manual/en/splfileobject.seek.php](http://php.net/manual/en/splfileobject.seek.php)