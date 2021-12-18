# PHP|Gmagick scaleimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-scaleimage-function/](https://www.geeksforgeeks.org/php-gmagick-scaleimage-function/)

**gmagick：：scaleimage()**函数是 PHP 中的一个内置函数，用于将图像大小缩放到给定的尺寸。
**语法：**和

```php
*Gmagick* Gmagick::scaleimage( $width, $height, $fit = FALSE )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$width：**该参数用于设置图片的宽度。
*   **$Height：**该参数用于设置图像的高度。

**返回值：**此函数成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：scaleImage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Scale the image.
$gmagick->scaleimage(400, 800, TRUE);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/da82429f866130aebc71b700c7250d1c.png)

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

// Scale the image
$gmagick->scaleimage(450, 900, FALSE);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/789d2995af74ffd18891186175fea6b0.png)

**引用：**[http://php.net/manual/en/gmagick.scaleimage.php](http://php.net/manual/en/gmagick.scaleimage.php)