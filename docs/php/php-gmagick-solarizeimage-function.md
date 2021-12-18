# PHP|Gmagick solarizeimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-solarizeimage-function/](https://www.geeksforgeeks.org/php-gmagick-solarizeimage-function/)

**gmagick：：solarizeimage()**函数是 PHP 中的内置函数，用于应用图像上的日光效果。 在照片暗室中，通过选择性地将感光纸区域暴露在光中而获得的图像效果。语法：和
。
**语法：**和

```php
*Gmagick* Gmagick::solarizeimage ( $threshold )
```

**参数：**此函数接受单个参数*$Threshold*，该参数用于测量日晒程度。
**返回值：**此函数在成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时抛出 GmagickException。
下面的程序说明了 PHP 中的**Gmagick：：solarizeimage()**函数：
**程序 1：**和
**输入图像**和

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Solarize the image.
$gmagick->solarizeimage(10);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```