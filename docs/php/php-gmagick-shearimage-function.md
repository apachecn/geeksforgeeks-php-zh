# PHP|Gmagick shearimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-shearimage-function/](https://www.geeksforgeeks.org/php-gmagick-shearimage-function/)

**Gmagick：：shearimage()**函数是 PHP 中的一个内置函数，用于沿 X 或 Y 轴滑动图像的一条边以创建平行四边形。 X 方向的剪切沿 X 轴滑动边，而 Y 方向的剪切沿 Y 轴滑动边。 剪切角度用于设置图像的剪切。
**语法：**和

```php
*Gmagick* Gmagick::shearimage( $color, $xShear, $yShear )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$COLOR：**此参数用于设置背景颜色。
*   **$xSear：**此参数用于设置图像的 x 向剪切度数。
*   **$ySear：**此参数用于设置图像的 y 向剪切度数。

**返回值：**此函数在成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：shearImage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// shear the image.
$gmagick->shearimage('blue', 25, 50);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/8f6c96c19cc2d599efbc578b165c0d34.png)

**程序 2：**和

## PHP

```php
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

// Shear the image
$gmagick->shearimage('yellow', 20, 40);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/8e08a9241867f4cc8efbed9a52a6b739.png)

**引用：**[http://php.net/manual/en/gmagick.shearimage.php](http://php.net/manual/en/gmagick.shearimage.php)