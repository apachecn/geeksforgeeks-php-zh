# PHP|SplFileInfo getCTime()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getctime-function/](https://www.geeksforgeeks.org/php-splfileinfo-getctime-function/)

SplFileInfo：：getCTime()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取 inode 更改时间。 返回时间采用 Unix 时间戳格式。

**语法：**

```php
*int* SplFileInfo::getCTime( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Unix 时间戳格式的时间。

下面的程序演示了 PHP 中的 SplFileInfo：：getCTime()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getCTime() function

$file = new SplFileInfo("gfg.txt");

$gfg = $file->getCTime();
echo date("F d Y H:i:s.", $gfg);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// PHP program to use array to check
// multiple files
$GFG = array (
    "dummy.php",
    "frame.php",
    "gfg.txt",
    "dummy.php"
);

foreach ($GFG as &$file_name) {

    // Create new SplFile Object
    $file = new SplFileInfo($file_name);

    // Print result
    $gfg = $file->getCTime();
    echo date("F d Y H:i:s.", $gfg). "</br>"; 
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.getctime.php](http://php.net/manual/en/splfileinfo.getctime.php)