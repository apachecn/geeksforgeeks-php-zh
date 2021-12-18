# PHP|Imagick getImageColors()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagecolors-function/](https://www.geeksforgeeks.org/php-imagick-getimagecolors-function/)

**Imagick：：getImageColors()**函数是 PHP 中的一个内置函数，用于获取图像中唯一颜色的数量。

**语法：**

```
*int* Imagick::getImageColors( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，用于确定图像中唯一颜色的数量。

**错误/异常：**它在出错时抛出 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageColors()**函数：

**程序：**

## PHP

```
<?php
//require_once('path/vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-14.png");

// getImageColors function
$size = $image->getImageColors();

// Display the unique color
print_r($size);
?>
```

发帖主题：Re：Колибри0.7.0

```
2955

```

**相关文章：**

*   [PHP|Imagick AdaptiveThresholdImage()函数](https://www.geeksforgeeks.org/php-imagickadaptivethresholdimage-function/)
*   [PHP|Imagick transverseImage()函数](https://www.geeksforgeeks.org/php-imagick-transverseimage-function/)

**引用：**[http://php.net/manual/en/imagick.getimagecolors.php](http://php.net/manual/en/imagick.getimagecolors.php)