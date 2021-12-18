# PHP|SplFileObject ftell()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-ftell-function/](https://www.geeksforgeeks.org/php-splfileobject-ftell-function/)

Fell()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于返回指定文件中当前偏移量的文件指针的位置。

**语法：**

```php
*int* SplFileObject::ftell( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件指针的位置。

下面的程序演示了 PHP 中的 SplFileObject：：fell()函数：

**程序 1：**

```php
<?php

// Create an Spl Object
$file = new SplFileObject("gfg.txt");

// Read line from file
$data = $file->fgets();

// Print position 
echo $file->ftell();
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

// Loop to read each file
foreach ($GFG as &$arr) {

    // Creating Spl Object
    $file = new SplFileObject($arr);

    // Function to read first line
    $data = $file->fgets();

    // Display result
    echo $file->ftell() . "</br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileobject.ftell.php](http://php.net/manual/en/splfileobject.ftell.php)