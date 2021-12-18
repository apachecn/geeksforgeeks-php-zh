# PHP|SplFileObject fwrite()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fwrite-function/](https://www.geeksforgeeks.org/php-splfileobject-fwrite-function/)

Fwrite()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于写入文件。

**语法：**

```php
*int* SplFileObject::fwrite( $str, $length )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$str:** it is used to specify the string that needs to be written to the file.
*   **$Length:** optional parameters. If given, file writing stops after the specified length.

**返回值：**此函数返回写入文件的字节数，出错时返回 0。

下面的程序演示了 PHP 中的 SplFileObject：：fwrite()函数：

**程序 1：**

```php
<?php

// Create a file named "gfg.txt" if not exist
$gfg = new SplFileObject("gfg.txt", "w+");

// Write data in gfg.txt
$gfg->fwrite("GeeksforGeeks a CS Portal");

// Open file again in read mode
$gfg = new SplFileObject("gfg.txt");

// Print result after written
while (!$gfg->eof()) {
    echo $gfg->fgetc();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create an Array
$GFG = array(
    "dummy.txt",
    "gfg.txt",
    "frame.txt"
    );

// Creating Spl Object
foreach ($GFG as &$arr) {
    $gfg = new SplFileObject($arr, "w+");

    // Write data in file
    $gfg->fwrite("GeeksforGeeks a CS Portal for Geeks");

    // Open file again in read mode
    $gfg = new SplFileObject("gfg.txt");

    // Print result after written
    while (!$gfg->eof()) {
        echo $gfg->fgetc();
    }

    echo  "</br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileobject.fwrite.php](http://php.net/manual/en/splfileobject.fwrite.php)