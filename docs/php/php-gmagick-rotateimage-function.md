# PHP|Gmagick rotateimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-rotateimage-function/](https://www.geeksforgeeks.org/php-gmagick-rotateimage-function/)

**Gmagick：：rotateImage()**函数是 PHP 中的一个内置函数，用于以指定的度数旋转图像。 背景用背景颜色填充的空三角形。
**语法：**和

```
*Gmagick* Gmagick::rotateimage ( $color, $degrees )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$COLOR：**此参数用于设置背景颜色像素。
*   **$Degrees：**此参数用于设置旋转度数。

**返回值：**此函数在成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：rotateImage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Rotate the image.
$gmagick->rotateimage('red', 35);

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/da22ea6e97c3b31e90aa120af36f1ccb.png)

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

// Create a GmagickDraw object
$gmagick = new Gmagick();

// Function to create new image of given size
$gmagick->newImage(500, 500, 'White');

// Function to set image format
$gmagick->setImageFormat("png");

// Function to draw image
$gmagick->drawImage($draw);

// Rotate the image
$gmagick->rotateimage('yellow', 35);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/7196521868e533f5514520259ad47c19.png)

**引用：**[http://php.net/manual/en/gmagick.rotateimage.php](http://php.net/manual/en/gmagick.rotateimage.php)