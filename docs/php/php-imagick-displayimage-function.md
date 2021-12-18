# PHP|Imagick displayImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-displayimage-function/](https://www.geeksforgeeks.org/php-imagick-displayimage-function/)

**Imagick：：displayImage()**函数是 PHP 中的内置函数，用于显示图像对象。

**语法：**

```
*bool* Imagick::displayImage( $servername )
```

**参数：**此函数接受用于指定服务器名称的单个参数*$servername*。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：displayImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use displayImage function
$imagick->displayImage(5);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![oil paint image](img/514879b60418370e73beb5515598d8c2.png)

**程序 2：**

```
<?php
$string = "Computer Science portal for Geeks!";

// creating new image of above String 
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

$im->setImageFormat('jpeg');

header("Content-Type: image/jpg");

// Display the output image
echo $im->getImageBlob();
?>
```

**输出：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

**引用：**[http://php.net/manual/en/imagick.displayimage.php](http://php.net/manual/en/imagick.displayimage.php)