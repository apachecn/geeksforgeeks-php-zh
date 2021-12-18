# PHP|SplFileInfo getSize()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getsize-function/](https://www.geeksforgeeks.org/php-splfileinfo-getsize-function/)

SplFileInfo：：getSize()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件大小(以字节为单位)。

**语法：**

```php
*int* SplFileInfo::getSize( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件大小(以字节为单位)。

下面的程序演示了 PHP 中的 SplFileInfo：：getSize()函数。

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo getSize function

$file = new SplFileInfo("gfg.txt");
$gfg = $file->getSize();

// Print real path if exist
print($gfg . "</br>");

$file = new SplFileInfo(__FILE__);
$gfg = $file->getSize();

// Print real path if exist
print($gfg);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// PHP program to use array to check multiple files
$GFG = array (
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg_code.cpp",
    "/var/www/html/gfg.txt",
    "frame.php"
);

foreach ($GFG as &$file_name) {

    // create new SplFile Object
    $file = new SplFileInfo($file_name);

    $gfg = $file->getSize();

    // Print real path if exist
    print($gfg. "</br>");
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.getsize.php](http://php.net/manual/en/splfileinfo.getsize.php)