# PHP|Gmagick Cropthhumnailimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-cropthumbnailimage-function/](https://www.geeksforgeeks.org/php-gmagick-cropthumbnailimage-function/)

**Gmagick：：cropthhumnailimage()**函数是 PHP 中的一个内置函数，用于通过缩小图像，然后从中心裁剪指定区域来创建固定大小的缩略图。
**语法：**和

```
*Gmagick* Gmagick::cropthumbnailimage( $width, $height )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$width：**该参数用于设置缩略图的宽度。
*   **$Height：**该参数用于设置缩略图的高度。

**返回值：**此函数返回裁剪的 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
以下程序说明 PHP：
**程序 1：**和
**原始图像：**和
中的**Gmagick：：cropthhumnailimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Use cropthumbnailimage() function
$gmagick->cropthumbnailimage(300, 600);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/5df21a04c09aa0a0256c0eab4a197f82.png)

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

// Use cropthumbnailimage() function
$gmagick->cropthumbnailimage(300, 100);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/9197c2a219567e0a3361cbf2c97bd1ab.png)

**引用：**[http://php.net/manual/en/gmagick.cropthumbnailimage.php](http://php.net/manual/en/gmagick.cropthumbnailimage.php)