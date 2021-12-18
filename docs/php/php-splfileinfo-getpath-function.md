# PHP|SplFileInfo getPath()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getpath-function/](https://www.geeksforgeeks.org/php-splfileinfo-getpath-function/)

SplFileInfo：：getPath()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于返回不带文件名的路径。

**语法：**

```php
*string* SplFileInfo::getPath( void )
```

**参数**：该函数不接受任何参数。

**返回值**：此函数返回不含文件名的文件路径。

下面的程序演示了 PHP 中的 SplFileInfo：：getPath()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getPath() function

// Create new SPlFileInfo Object
$file = new SplFileInfo("html/gfg.txt");

// Print result
echo $file->getPath();

?>
```

**Output:**

```php
html

```

**程序 2：**

```php
<?php

// PHP program to check multiple files path

$GFG = array (
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg.txt",
    "/var/www/html/gfg.php",
    "dummy.php"
);

foreach ($GFG as &$file_name) {

    // Create new SplFile Object
    $file = new SplFileInfo($file_name);

    // Print result
    echo $file->getPath() . "</br>";

}
?>
```

**Output:**

```php
/home/rajvir/Desktop/GeeksforGeeks
/home/rajvir/Desktop
/var/www/html

```

**引用：**[http://php.net/manual/en/splfileinfo.getpath.php](http://php.net/manual/en/splfileinfo.getpath.php)