# PHP|Gmagick Normizeimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-normalizeimage-function/](https://www.geeksforgeeks.org/php-gmagick-normalizeimage-function/)

**Gmagick：：Normizeimage()**函数是 PHP 中的一个内置函数，用于通过调整像素的颜色以跨越整个颜色范围来增强彩色图像的对比度。

**语法：**

```php
*Gmagick* Gmagick::normalizeimage( $channel )
```

参数
**：**此函数接受单个参数*$CHANNEL*。 此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Gmagick 函数中的默认通道是 Gmagick：：Channel_Default。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：Normal izeImage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Normalize the image. 
$gmagick->normalizeimage(Gmagick::CHANNEL_YELLOW);

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/d32797ea3e1469516cc03115555dc3c3.png)

**程序 2：**

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

// Normalize the image. 
$gmagick->normalizeimage(Gmagick::CHANNEL_ALL);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/a44dde21464ac5e13b942dee812bd0fe.png)
**参考：**[http://php.net/manual/en/gmagick.normalizeimage.php](http://php.net/manual/en/gmagick.normalizeimage.php)