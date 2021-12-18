# PHP|SplFileInfo getPathname()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getpathname-function/](https://www.geeksforgeeks.org/php-splfileinfo-getpathname-function/)

SplFileInfo：：getPathname()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件路径。

**语法：**

```
*string* SplFileInfo::getPathname( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件的路径。

下面的程序演示了 PHP 中的 SplFileInfo：：getPathname()函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// SplFileInfo::getPathname() function

$file = new SplFileInfo('/var/www/html/gfg.php');

$info = $file->getPathname();
print_r($info);

?>
```

**Output:**

```
/var/www/html/gfg.php

```

**程序 2：**

```
<?php

// PHP program to use array to check
// multiple files path

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
    $info = $file->getPathname();
    print_r($info);
    echo "</br>";
}
?>
```

**Output:**

```
/home/rajvir/Desktop/GeeksforGeeks/dummy.php
/home/rajvir/Desktop/gfg.txt
/var/www/html/gfg.php
dummy.php

```

**引用：**[http://php.net/manual/en/splfileinfo.getpathname.php](http://php.net/manual/en/splfileinfo.getpathname.php)