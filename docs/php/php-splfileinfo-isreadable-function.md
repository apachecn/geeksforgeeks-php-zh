# PHP|SplFileInfo isReadable()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-isreadable-function/](https://www.geeksforgeeks.org/php-splfileinfo-isreadable-function/)

SplFileInfo：：isReadable()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于检查给定文件是否可读。

**语法：**

```
*bool* SplFileInfo::isReadable( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**注意：**在执行程序之前设置文件权限。

下面的程序演示了 PHP 中的 SplFileInfo：：isReadable()函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo::isReadable() function

$file = new SplFileInfo("gfg.txt");
$gfg = $file->isReadable();

// Print result
var_dump($gfg);
echo "</br>";

$file = new SplFileInfo(__FILE__);
$gfg = $file->isReadable();

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
    "dummy.php",
    "gfg_code.cpp",
    "html/",
    "frame.php"
);

foreach ($GFG as &$file_name) { 

    // Create new SplFile Object 
    $file = new SplFileInfo($file_name); 

    $gfg = $file->isReadable();

    // Print result
    var_dump($gfg);
    echo "</br>";

} 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.isreadable.php](http://php.net/manual/en/splfileinfo.isreadable.php)