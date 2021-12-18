# PHP|SplFileInfo getPerms()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getperms-function/](https://www.geeksforgeeks.org/php-splfileinfo-getperms-function/)

SplFileInfo：：getPerms()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的权限。

**语法：**

```
*int* SplFileInfo::getPerms( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 file 的权限。

下面的程序演示了 PHP 中的 SplFileInfo：：getPerms()函数：

[]T2→程序 1：ΔT3？

ΔT0？→T1]*

**示例 2：**

```
<?php

// PHP program to use array to check multiple files
$GFG = array (
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "/home/rajvir/Desktop/gfg_code.cpp",
    "/var/www/html/gfg.php",
    "dummy.php"
);

foreach ($GFG as &$file_name) {

    // Create new SplFile Object
    $file = new SplFileInfo($file_name);

    $gfg = $file->getPerms();

    // Print permission in octal form
    echo substr(sprintf('%o', $gfg), -3) . "</br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileinfo.getperms.php](http://php.net/manual/en/splfileinfo.getperms.php)