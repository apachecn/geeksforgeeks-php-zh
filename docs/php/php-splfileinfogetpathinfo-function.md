# PHP|SplFileInfo：：getPathInfo()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfogetpathinfo-function/](https://www.geeksforgeeks.org/php-splfileinfogetpathinfo-function/)

SplFileInfo：：getPathInfo()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取路径的 SplFileInfo 对象。
**语法：**和

```
SplFileInfo::getPathInfo( $class )
```

**参数：**此函数接受可选的单个参数*$class*。 用于指定 SplFileInfo 派生类名的名称。
**返回值**：此函数返回文件父路径的 SplFileInfo 对象。
下面的程序说明了 SplFileInfo：：getPathInfo()函数。
**程序 1：**和

## PHP

```
<?php

// PHP Program to illustrate
// Splfileinfo getPathInfo function

$file = new SplFileInfo('/var/www/html/gfg.php');

$info = $file->getPathInfo();
print_r($info);

?>
```

**Output:** 

```
SplFileInfo Object
(
    [pathName:SplFileInfo:private] => /var/www/html
    [fileName:SplFileInfo:private] => html
)
```

**程序 2：**和

## PHP

```
<?php

// Use array to check multiple
// files path

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
    $info = $file->getPathInfo();
    print_r($info);
    echo "</br>";
}
?>
```

**Output:** 

```
SplFileInfo Object
(
    [pathName:SplFileInfo:private] => /home/rajvir/Desktop/GeeksforGeeks
    [fileName:SplFileInfo:private] => GeeksforGeeks
)

SplFileInfo Object
(
    [pathName:SplFileInfo:private] => /home/rajvir/Desktop
    [fileName:SplFileInfo:private] => Desktop
)

SplFileInfo Object
(
    [pathName:SplFileInfo:private] => /var/www/html
    [fileName:SplFileInfo:private] => html
)

SplFileInfo Object
(
    [pathName:SplFileInfo:private] => .
    [fileName:SplFileInfo:private] => .
)
```

**引用：**[http://php.net/manual/en/splfileinfo.getpathinfo.php](http://php.net/manual/en/splfileinfo.getpathinfo.php)