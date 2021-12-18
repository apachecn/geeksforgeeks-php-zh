# PHP|SplFileObject ftruncate()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-ftruncate-function/](https://www.geeksforgeeks.org/php-splfileobject-ftruncate-function/)

SplFileObject：：ftruncate()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于截断以字节为单位的文件大小。

**语法：**

```
*bool* SplFileObject::ftruncate( $length )
```

**参数：**此函数接受指定文件截断长度的单个参数*$length*。

**返回值：**此函数成功时返回 True，失败时返回 False。

以下程序说明了 PHP 中的 SplFileObject ftruncate()函数：

**程序 1：**

```
<?php

// Create a file named "gfg.txt" which
// containing data "GeeksforGeeks"
$gfg = new SplFileObject("gfg.txt", "w+");
$gfg->fwrite("GeeksforGeeks");

// Truncate file 
$gfg->ftruncate(8);

// Rewind and reading data from file
$gfg->rewind();

// Print result after truncate
echo $gfg->fgets();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create an Array
$GFG = array(
    "dummy.txt",
    "gfg.txt",
    "frame.txt"
    );

// Creating Spl Object
foreach ($GFG as &$arr) {
    $file = new SplFileObject($arr);

    // Truncate file 
    $file->ftruncate(8);

    // Rewind and reading data from file
    $file->rewind();

    // Print result after truncate
    echo $file->fgets();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileobject.ftruncate.php](http://php.net/manual/en/splfileobject.ftruncate.php)