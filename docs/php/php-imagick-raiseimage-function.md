# PHP|Imagick riseImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-raiseimage-function/](https://www.geeksforgeeks.org/php-imagick-raiseimage-function/)

**Imagick：：Rise eImage()**函数是 PHP 中的一个内置函数，用于通过闪电和使图像边缘变暗来创建模拟的三维按钮效果。
**语法：**

```php
*bool* Imagick::raiseImage( $width, $height, $x, $y, $raise )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$width：**此参数存储按钮的宽度值。
*   **$Height：**此参数存储按钮高度的值。
*   **$x：**此参数存储 x 坐标的值。
*   **$y：**此参数存储 y 坐标的值。
*   **$RAISE：**此参数存储所需提升量的值。

**返回值：**成功时此函数返回 True。
**原图：**和

![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

下面的程序说明 PHP 中的**Imagick Rise Image()**函数：
**程序 1：**

## PHP

```php
<?php

// require_once('path/vendor/autoload.php');
header('Content-type: image/png');

// Create new Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use raiseImage function
$image->raiseImage(20,30,10,15,25);

// Display the image
echo $image;
?>
```

发帖主题：Re：Колибри0.7.0

![](img/f907194f994910ae4649db6f87c60b62.png)

**程序 2：**

## PHP

```php
<?php

$string = "Computer Science portal for Geeks!";

// Creating new image of above String
// and add color and background
$im = new Imagick();

$draw = new ImagickDraw();

// Fill the color in image
$draw->setFillColor(new ImagickPixel('green'));

// Set the text font size
$draw->setFontSize(50);

$metrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($metrix['textWidth'], $metrix['textHeight'],
new ImagickPixel('white'));

// Draw the image        
$im->drawImage($draw);

// raiseImage Function
$im->raiseImage(5,15,50,25,20);

$im->setImageFormat('jpeg');

header("Content-Type: image/jpg");

// Display the output image
echo $im->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/8a3cbdc6ac408e2dbfb753055d5cd101.png)

**引用：**[http://php.net/manual/en/imagick.raiseimage.php](http://php.net/manual/en/imagick.raiseimage.php)