# PHP|Gmagick enhanceimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-enhanceimage-function/](https://www.geeksforgeeks.org/php-gmagick-enhanceimage-function/)

**Gmagick：：enhanceimage()**函数是 PHP 中的一个内置函数，用于改善噪声图像的质量。 此功能应用数字滤波器来提高质量。
**语法：**和

```
*Gmagick* Gmagick::enhanceimage( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回增强的 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
以下程序说明 PHP：
**程序 1：**和
**原始图像：**和
中的**Gmagick：：enhanceimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Enhance the image.
$gmagick->enhanceimage();

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```