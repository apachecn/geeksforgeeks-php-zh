# PHP|SplFileInfo getFilename()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getfilename-function/](https://www.geeksforgeeks.org/php-splfileinfo-getfilename-function/)

SplFileInfo：：getFilename()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件名。

**语法：**

```php
*string* SplFileInfo::getFilename( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件名的字符串。

下面的程序演示了 PHP 中的 SplFileInfo：：getFilename()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getFilename() function

// Create new SPlFileInfo Object
$file = new SplFileInfo("gfg.txt");

// Print result

echo( $file->getFilename());
?>
```

**Output:**

```php
gfg.txt

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
    "demo.c"
);

foreach ($GFG as $file_name) {

    // Create new SPlFileInfo Object
    $file = new SplFileInfo($file_name);

    // Print result
    echo($file->getFilename());
    echo "</br>";
}
?>
```

**Output:**

```php
dummy.php
gfg.txt
gfg.php
demo.c

```

**参考**：[http://php.net/manual/en/splfileinfo.getfilename.php](http://php.net/manual/en/splfileinfo.getfilename.php)