# PHP|Gmagick Embossimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-embossimage-function/](https://www.geeksforgeeks.org/php-gmagick-embossimage-function/)

**gmagick：：embossimage()**函数是 PHP 中的一个内置函数，用于返回具有三维效果的灰度图像。 该函数使用给定半径和标准差的高斯算子对图像进行过滤。
**语法：**和

```
*Gmagick* Gmagick::embossimage( $radius, $sigma )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$RADIUS：**此参数保存半径效果的值。
*   **$sigma：**此参数保存 sigma 效应值。

**返回值：**此函数返回浮雕的 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**原始图像：**和
中的**Gmagick：：Embossimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Emboss the image.
$gmagick->embossimage(12, 5);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/dd5f866a59168a7172428b56edd404aa.png)

**程序 2：**和

## PHP

```
<?php

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Create GmagickPixel object
$strokeColor = new GmagickPixel('Red');
$fillColor = new GmagickPixel('Green');

// Set the color, opacity of image
$draw->setStrokeOpacity(1);
$draw->setStrokeColor('Red');
$draw->setFillColor('Green');

// Set the width and height of image
$draw->setStrokeWidth(7);
$draw->setFontSize(72);

// Function to draw circle 
$draw->circle(250, 250, 100, 150);

$gmagick = new Gmagick();
$gmagick->newImage(500, 500, 'White');
$gmagick->setImageFormat("png");
$gmagick->drawImage($draw);

// Emboss the image.

$gmagick->embossimage(15, 6);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/321c25eb2301539b8be2d9bd7624ffa6.png)

**引用：**[http://php.net/manual/en/gmagick.embossimage.php](http://php.net/manual/en/gmagick.embossimage.php)