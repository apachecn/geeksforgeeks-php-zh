# PHP|SplFileInfo getBasename()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getbasename-function/](https://www.geeksforgeeks.org/php-splfileinfo-getbasename-function/)

SplFileInfo：：getBasename()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的基本名称。

**语法：**

```php
*string* SplFileInfo::getBasename( $suffix )
```

**参数：**此函数接受可选的单个参数*$suffix*。 它用于指定基本名称。

**返回值：**此函数返回不带路径信息的基本名称。

下面的程序演示了 PHP 中的 SplFileInfo：：getBasename()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getBasename() function

// Create new SPlFileInfo Object
$file = new SplFileInfo('html/gfg.txt');

// Print result
var_dump($file->getBasename());
?>
```

**输出：**

```php
string(7) "gfg.txt"

```

**程序 2：**

```php
<?php

// PHP program to use array to check
// multiple files
$GFG = array (
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg.txt",
    "/var/www/html/gfg.php",
    "demo.php"
);

foreach ($GFG as &$file) {

    // Create new SPlFileInfo Object
    $file = new SplFileInfo($file);

    // Print result
    var_dump($file->getBasename());

}
?>
```

**输出：**

```php
string(9) "dummy.php"
string(7) "gfg.txt"
string(7) "gfg.php"
string(8) "demo.php"

```

**引用：**[http://php.net/manual/en/splfileinfo.getbasename.php](http://php.net/manual/en/splfileinfo.getbasename.php)