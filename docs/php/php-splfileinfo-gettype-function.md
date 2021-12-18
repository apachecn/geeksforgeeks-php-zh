# PHP|SplFileInfo getType()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-gettype-function/](https://www.geeksforgeeks.org/php-splfileinfo-gettype-function/)

SplFileInfo：：getType()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件类型。

**语法：**

```
*string* SplFileInfo::getType( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件类型，即链接、目录或文件。

下面的程序演示了 PHP 中的 SplFileInfo：：getType()函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo::getType() function

$file = new SplFileInfo(dirname("gfg.txt"));
$gfg = $file->getType();

// Print result
print($gfg . "</br>");

$file = new SplFileInfo(__FILE__);
$gfg = $file->getType();

// Print result
print($gfg);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
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

    // Print result 
    echo $file->getType() . "</br>"; 

} 
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.gettype.php](http://php.net/manual/en/splfileinfo.gettype.php)