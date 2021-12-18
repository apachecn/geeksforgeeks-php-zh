# PHP|SplFileInfo getExtension()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getextension-function/](https://www.geeksforgeeks.org/php-splfileinfo-getextension-function/)

SplFileInfo：：getExtension()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件扩展名。

**语法：**

```
*string* SplFileInfo::getExtension( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件扩展名的字符串。

下面的程序演示了 PHP 中的 SplFileInfo：：getExtension 函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo getExtension function

// Create new SPlFileInfo Object
$file = new SplFileInfo("gfg.php");

// Print result
echo $file->getExtension();
?>
```

**Output:**

```
php

```

**程序 2：**

```
<?php

// PHP program to use array to check
// multiple files
$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg.txt",
    "/var/www/html/gfg.php",
    "demo.c"
);

foreach ($GFG as &$file_name) {

    // Create new SPlFileInfo Object
    $file = new SplFileInfo($file_name);

    // Print result
    echo $file->getExtension() . "</br>";
}
?>
```

**Output:**

```
php
txt
php
c

```

**引用：**[http://php.net/manual/en/splfileinfo.getextension.php](http://php.net/manual/en/splfileinfo.getextension.php)