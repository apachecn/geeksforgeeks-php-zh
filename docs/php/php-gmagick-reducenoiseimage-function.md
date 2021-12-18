# PHP|Gmagick Reducenoiseimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-reducenoiseimage-function/](https://www.geeksforgeeks.org/php-gmagick-reducenoiseimage-function/)

**Gmagick：：Reducenoiseimage()**函数是 PHP 中的一个内置函数，用于设置图像的平滑轮廓，同时仍然保留边缘信息。 该算法的工作原理是将每个像素替换为其相邻的最近值。
**语法：**和

```php
*Gmagick* Gmagick::reducenoiseimage( $radius )
```

**参数：**此函数接受单个参数*$Radius*，该参数用于设置邻域像素的半径。
**返回值：**此函数成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时抛出 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：Reducenoiseimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Reduce Noise in the image.
$gmagick->reducenoiseimage(7);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```