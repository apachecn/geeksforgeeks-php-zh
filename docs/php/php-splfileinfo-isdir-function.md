# PHP|SplFileInfo isDir()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-isdir-function/](https://www.geeksforgeeks.org/php-splfileinfo-isdir-function/)

SplFileInfo：：isDir()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于检查文件是否为目录。

**语法：**

```php
*bool* SplFileInfo::isDir( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果 file 是目录，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 SplFileInfo：：isDir()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::isDir() function

$file = new SplFileInfo(dirname("gfg.txt"));
$gfg = $file->isDir();

// Print result
var_dump($gfg);
echo "</br>";

$file = new SplFileInfo(__FILE__);
$gfg = $file->isDir();

// Print result
var_dump($gfg);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php 

// PHP program to use array to check 
// multiple files 

$GFG = array (
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop",
    "/var/www/html/",
    "frame.php"
);

foreach ($GFG as &$file_name) { 

    // Create new SplFile Object 
    $file = new SplFileInfo($file_name); 

    $gfg = $file->isDir();

    // Print result
    var_dump($gfg);
    echo "</br>";
} 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.isdir.php](http://php.net/manual/en/splfileinfo.isdir.php)