# PHP|Imagick getImageColorspace()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagecolorspace-function/](https://www.geeksforgeeks.org/php-imagick-getimagecolorspace-function/)

**Imagick：：getImageColorspace()**函数是 PHP 中的一个内置函数，用于获取图像的色彩空间。 颜色空间是一个数学模型，它将颜色范围描述为数字元组，通常为 3 或 4 个值或颜色分量(RGB)。

**语法：**

```php
*int* Imagick::getImageColorspace( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回一个整数值，可以与颜色空间常量进行比较。

**错误/异常：**它在出错时抛出 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageColorspace()**函数：

**程序：**

```php
<?php 
// require_once('path/vendor/autoload.php'); 

// Create a new Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-14.png');

// getImageColorspace function
$size = $image->getImageColorspace();

// Display the colorspace
print_r($size);
?>
```

发帖主题：Re：Колибри0.7.0

```php
13
```

**相关文章：**

*   [PHP|Imagick borderImage()函数](https://www.geeksforgeeks.org/php-imagick-borderimage-function/)
*   [PHP|Imagick appendImages()函数](https://www.geeksforgeeks.org/php-imagick-appendimages-function/)

**引用：**[http://php.net/manual/en/imagick.getimagecolorspace.php](http://php.net/manual/en/imagick.getimagecolorspace.php)