# PHP|Gmagick oilpatimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-oilpaintimage-function/](https://www.geeksforgeeks.org/php-gmagick-oilpaintimage-function/)

**Gmagick：：oilpatimage()**函数是 PHP 中的一个内置函数，用于应用模拟油画的特殊效果滤镜。 此函数应用模拟油画的特殊效果滤镜。 此函数用半径定义的圆形区域中出现的最频繁的颜色替换每个像素。

**语法：**

```php
*Gmagick* Gmagick::oilpaintimage( $radius )
```

参数
**：**此函数接受单个参数*$RADIUS*。 用于设置圆形邻域的半径。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

下面的程序说明了 PHP 中的**Gmagick：：Oilpatimage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Give OilPaint Effect to the image. 
$gmagick->oilpaintimage(15);

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/3e8acce888c75ee6b3eeb6bb83d051cb.png)

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

// Give OilPaint Effect to the image 
$gmagick->oilpaintimage(20);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/b61d749ded5afc9055a961a290ab5d2b.png)

**引用：**[http://php.net/manual/en/gmagick.oilpaintimage.php](http://php.net/manual/en/gmagick.oilpaintimage.php)