# PHP|Gmagick borderImage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-borderimage-function/](https://www.geeksforgeeks.org/php-gmagick-borderimage-function/)

**Gmagick：：borderImage()**函数是 PHP 中的一个内置函数，用于在图像中绘制边框。 此函数用于在给定颜色的图像周围创建边框。

**语法：**

```
*Gmagick* Gmagick::borderImage( $bordercolor, $width, $height )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$borderColor：**此参数保存包含边框颜色的字符串。
*   **$width：**此参数用于设置边框宽度。
*   **$Height：**该参数用于设置边框高度。

**返回值：**此函数成功时返回 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：borderImage()**函数：

**程序 1：**

```
<?php

// Create an image object
$image = new Gmagick (
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Set the border in the given image
$image->borderImage('green', 100, 100);

header("Content-Type: image/jpg");

// Display image
echo $image;
?>
```

**输出：**
![border image](img/8dc6ac54ab8dbdf84f4ed135c502a6a3.png)

**程序 2：**

```
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color and background 
$im = new Gmagick(); 
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

// Set the border in the given image
$image->borderImage('green', 20, 20);

header("Content-Type: image/jpg");

// Display image
echo $image;
?>
```

**输出：**
![border image](img/4ed4b10cfa0946d5f167066649930139.png)

**引用：**[http://php.net/manual/en/gmagick.borderimage.php](http://php.net/manual/en/gmagick.borderimage.php)