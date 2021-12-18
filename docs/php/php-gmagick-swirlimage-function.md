# PHP|Gmagick swirlimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-swirlimage-function/](https://www.geeksforgeeks.org/php-gmagick-swirlimage-function/)

**Gmagick：：swirlimage()**函数是 PHP 中的一个内置函数，用于围绕图像中心旋转像素。 阶数表示移动每个像素的弧线扫描程度。
**语法：**和

```
*Gmagick* Gmagick::swirlimage( $degrees )
```

**参数：**此函数接受单个参数*$度*，该参数定义旋转效果的紧密程度。
**返回值：**此函数在成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时抛出 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：swirlimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Swirl the image.
$gmagick->swirlimage(200);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```