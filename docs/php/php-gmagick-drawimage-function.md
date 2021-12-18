# PHP|Gmagick draimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-drawimage-function/](https://www.geeksforgeeks.org/php-gmagick-drawimage-function/)

**Gmagick：：drawimage()**函数是 PHP 中的一个内置函数，用于在当前图像上呈现 GmagickDraw 对象。

**语法：**

```
*Gmagick* Gmagick::drawimage ( $GmagickDraw )
```

*
**参数：**此函数接受单个参数*$GmagickDraw*，该参数存储渲染图像的操作。

**返回值：**此函数返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

下面的程序说明了 PHP 中的**Gmagick：：drawImage()**函数：

**程序 1：**

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

// Use of drawimage function
$gmagick->drawimage($draw); 

// Emboss the image.

$gmagick->embossimage(15, 6);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/fa8c412997231bf12b49cff15a263548.png)

**程序 2：**

```
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw();  

// Set the color
$draw->setFillColor('Green'); 

// Set the width and height of image 
$draw->setStrokeWidth(7); 
$draw->setFontSize(72); 

// Function to draw rectangle  
$draw->rectangle(150, 150, 400, 400); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 

// Use of drawimage function
$gmagick->drawImage($draw); 

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/00edb98c79de3fc1bf1b1d63f22f80ea.png)

**引用：**[http://php.net/manual/en/gmagick.drawimage.php](http://php.net/manual/en/gmagick.drawimage.php)