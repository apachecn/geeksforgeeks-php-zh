# PHP|Imagick getColorspace()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getcolorspace-function/](https://www.geeksforgeeks.org/php-imagick-getcolorspace-function/)

**Imagick：：getColorspace()函数**是 PHP 中的一个内置函数，用于获取图像的全局色彩空间值。

**语法：**

```php
*int* Imagick::getColorspace( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，可以与[颜色空间常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.colorspace-undefined)进行比较。

下面的程序演示了 PHP 中的**Imagick：：getColorspace()函数**：

**程序：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Get the colorspace
$colorSpace = $imagick->getColorSpace();

// Display the colorspace
echo $colorSpace;

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getcolorspace.php](https://www.php.net/manual/en/imagick.getcolorspace.php)