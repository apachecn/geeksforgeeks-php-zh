# PHP|SplFileInfo getATime()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getatime-function/](https://www.geeksforgeeks.org/php-splfileinfo-getatime-function/)

SplFileInfo：：getATime()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的上次访问时间。

**语法：**

```php
*int* SplFileInfo::getATime( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件的最后访问时间。

下面的程序演示了 PHP 中的 SplFileInfo：：getATime()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getATime() function

// Create new SPlFileInfo Object
$file = new SplFileInfo('demo1.php');

// Print result
echo (date("F d Y H:i:s.", $file->getATime()));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// PHP program to use array to check multiple files

$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg.txt",
    "/var/www/html/gfg.php",
    "demo.php"
);

foreach ($GFG as &$file) {

    // Create new SPlFileInfo Object
    $file = new SplFileInfo('demo1.php');

    // Print result
    echo date("F d Y H:i:s.", $file->getATime()) . "</br>";

}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.getatime.php](http://php.net/manual/en/splfileinfo.getatime.php)