# PHP|Gmagick implodeimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-implodeimage-function/](https://www.geeksforgeeks.org/php-gmagick-implodeimage-function/)

**Gmagick：：implodeimage()**函数是 PHP 中的一个内置函数，用于创建一个新图像，该图像是现有图像的副本。 它使用按指定百分比内爆的图像像素。
**语法：**和

```php
*mixed* Gmagick::implodeimage( $radius )
```

**参数：**此函数接受保存内爆半径的单个参数*$Radius*。
**返回值：**此函数返回内爆的 Gmagick 对象。
**错误/异常：**此函数在出错时抛出 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：implodeimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Implode the image.
$gmagick->implodeimage(12);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```