# PHP|Gmagick stripimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-stripimage-function/](https://www.geeksforgeeks.org/php-gmagick-stripimage-function/)

**Gmagick：：stripimage()**函数是 PHP 中的一个内置函数，用于剥离图像中的所有配置文件和评论。

**语法：**

```php
*Gmagick* Gmagick::stripimage( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：stripimage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// strip the image. 
$gmagick->stripimage(); 

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/de911192396845789631ba406f0e976c.png)

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

// Strip the image
$gmagick->stripimage();

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/94e880f30068c18c5a11cb7395fad653.png)

**引用：**[http://php.net/manual/en/gmagick.stripimage.php](http://php.net/manual/en/gmagick.stripimage.php)