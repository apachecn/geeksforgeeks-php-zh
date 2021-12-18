# PHP|SplFileInfo getRealPath()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getrealpath-function/](https://www.geeksforgeeks.org/php-splfileinfo-getrealpath-function/)

SplFileInfo：：getRealPath()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取绝对文件路径。

**语法：**

```php
*int* SplFileInfo::getRealPath( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数在成功时返回文件的路径。

下面的程序演示了 PHP 中的 SplFileInfo：：getRealPath()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo getRealPath function

$file = new SplFileInfo("gfg.txt");
$gfg = $file->getRealPath();

// Print real path if exist
var_dump($gfg . "</br>");

$file = new SplFileInfo(__FILE__);
$gfg = $file->getRealPath();

// Print real path if exist
var_dump($gfg);

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
    "/var/www/html/gfg1.php",
    "dummy.php"
);

foreach ($GFG as &$file_name) {

    // Create new SplFile Object
    $file = new SplFileInfo($file_name);

    $gfg = $file->getRealPath();

    // Print real path if exist
    var_dump($gfg. "</br>");
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.getrealpath.php](http://php.net/manual/en/splfileinfo.getrealpath.php)