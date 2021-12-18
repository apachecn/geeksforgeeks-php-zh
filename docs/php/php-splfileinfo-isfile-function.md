# PHP|SplFileInfo isFile()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-isfile-function/](https://www.geeksforgeeks.org/php-splfileinfo-isfile-function/)

SplFileInfo：：isFile()函数是 PHP 标准 PHP 库(SPL)的内置函数，用于检查 SplFileInfo 对象是否为文件。

**语法：**

```
*bool* SplFileInfo::isFile( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果文件存在，此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 SplFileInfo：：isFile()函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo isFile function

$file = new SplFileInfo(dirname("gfg.txt"));
$gfg = $file->isFile();

// Print result
var_dump($gfg);
echo "</br>";

$file = new SplFileInfo(__FILE__);
$gfg = $file->isFile();

// Print result
var_dump($gfg);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php 

// PHP program to use array to check 
// multiple files 

$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg_code.cpp",
    "/var/www/html/",
    "frame.php"
);

foreach ($GFG as &$file_name) { 

    // Create new SplFile Object 
    $file = new SplFileInfo($file_name); 

    $gfg = $file->isFile();

    // Print result
    var_dump($gfg);
    echo "</br>";
} 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.isfile.php](http://php.net/manual/en/splfileinfo.isfile.php)