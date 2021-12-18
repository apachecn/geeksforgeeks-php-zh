# PHP|Imagick flopImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-flopimage-function/](https://www.geeksforgeeks.org/php-imagick-flopimage-function/)

**Imagick：：flopImage()**函数是 PHP 中的内置函数，用于创建水平镜像。

**语法：**

```
*bool* Imagick::flopImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

以下程序说明了 PHP 中的**Imagick：：flopImage()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using blueShiftImage function
$imagick->flopImage();

header("Content-Type: image/jpg");
echo $imagick->getImageBlob();

?>
```

发帖主题：Re：Колибри0.7.0

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/gfg_flopimage_before.png](img/6288b04bc479c274abd2b4fc53382521.png)

```
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
$im->setImageFormat('jpeg');

// using blueShiftImage function
$im->flopImage();

header("Content-Type: image/jpg");
echo $im->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

**引用：**[http://php.net/manual/en/imagick.flopimage.php](http://php.net/manual/en/imagick.flopimage.php)