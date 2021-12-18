# PHP|Imagick getImagePixelColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagepixelcolor-function/](https://www.geeksforgeeks.org/php-imagick-getimagepixelcolor-function/)

**Imagick：：getImagePixelColor()函数**是 PHP 中的内置函数，用于返回指定像素的颜色。

**语法：**

```php
*ImagickPixel* Imagick::getImagePixelColor( *int* $x, *int* $y )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$x:** it specifies the x coordinate of the pixel.
*   **$y:** it specifies the y coordinate of the pixel.

**返回值：**此函数返回给定坐标处颜色的 ImagickPixel 实例。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImagePixelColor()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Pixel Color
$colorPixel = $imagick->getImagePixelColor(300, 90);

// Convert Pixel into Color
$color = $colorPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Pixel Color
$colorPixel = $imagick->getImagePixelColor(0, 0);

// Convert Pixel into Color
$color = $colorPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagepixelcolor.php](https://www.php.net/manual/en/imagick.getimagepixelcolor.php)