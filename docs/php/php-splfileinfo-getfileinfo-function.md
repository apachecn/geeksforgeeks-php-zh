# PHP|SplFileInfo getFileInfo()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getfileinfo-function/](https://www.geeksforgeeks.org/php-splfileinfo-getfileinfo-function/)

SplFileInfo：：getFileInfo()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的文件信息。

**语法：**

```php
SplFileInfo::getFileInfo( $class )
```

**参数：**此函数接受可选的单个参数*$class*。 用于指定拆分文件派生类的名称。

**返回值：**此函数返回 SplFileInfo 对象。

下面的程序演示了 PHP 中的 SplFileInfo：：getFileInfo()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getFileInfo() function

// Create new SPlFileInfo Object
$file = new SplFileInfo("gfg.txt");

// Print result
var_dump( $file->getFileInfo());

?>
```

**Output:**

```php
object(SplFileInfo)#2 (2) {
  ["pathName":"SplFileInfo":private]=>
  string(7) "gfg.txt"
  ["fileName":"SplFileInfo":private]=>
  string(7) "gfg.txt"
}

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
    var_dump($file->getFileInfo());
    echo "</br>";
}
?>
```

**Output:**

```php
object(SplFileInfo)#2 (2) {
  ["pathName":"SplFileInfo":private]=>
  string(44) "/home/rajvir/Desktop/GeeksforGeeks/dummy.php"
  ["fileName":"SplFileInfo":private]=>
  string(9) "dummy.php"
}

object(SplFileInfo)#1 (2) {
  ["pathName":"SplFileInfo":private]=>
  string(28) "/home/rajvir/Desktop/gfg.txt"
  ["fileName":"SplFileInfo":private]=>
  string(7) "gfg.txt"
}

object(SplFileInfo)#2 (2) {
  ["pathName":"SplFileInfo":private]=>
  string(21) "/var/www/html/gfg.php"
  ["fileName":"SplFileInfo":private]=>
  string(7) "gfg.php"
}

object(SplFileInfo)#1 (2) {
  ["pathName":"SplFileInfo":private]=>
  string(6) "demo.c"
  ["fileName":"SplFileInfo":private]=>
  string(6) "demo.c"
}

```

**引用：**[http://php.net/manual/en/splfileinfo.getfileinfo.php](http://php.net/manual/en/splfileinfo.getfileinfo.php)