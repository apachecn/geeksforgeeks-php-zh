# PHP|SplFileObject Fread()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fread-function/](https://www.geeksforgeeks.org/php-splfileobject-fread-function/)

Fread()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于从文件中读取给定的字节数。

**语法：**

```php
*string* SplFileObject::fread( $length )
```

**参数：**此函数接受单个参数*$length*，该参数用于指定要从文件中读取的长度(以字节为单位)。

**返回值：**此函数成功时返回从文件读取的字符串，失败时返回 False。

**注意：**它确保名为 gfg.txt 的以下程序中使用的文件具有读取权限。

下面的程序演示了 PHP 中的 SplFileObject：：Fread()函数：

**程序 1：**

```php
<?php

// Create an Object 
$file = new SplFileObject("gfg.txt", "r");

// Read 5 bytes from file
$gfg = $file->fread(5);

// Print Result
echo ($gfg);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php 

// PHP program to use array to check 
// multiple files 
$GFG = array(
    "dummy.txt",
    "gfg.txt",
    "frame.txt"
    );

foreach ($GFG as &$file_name) { 

    // Create new SplFile Object 
    $file = new SplFileObject($file_name, "r");
    $contents = $file->fread(13);
    echo $contents . "</br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileobject.fread.php](http://php.net/manual/en/splfileobject.fread.php)