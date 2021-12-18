# PHP|Gmagick flopimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-flopimage-function/](https://www.geeksforgeeks.org/php-gmagick-flopimage-function/)

**Gmagick：：flopimage()**函数是 PHP 中的一个内置函数，用于创建失败的图像。 此函数用于沿 y 轴创建镜像。

**语法：**

```php
*Gmagick* Gmagick::flopimage( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回翻转的 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：flopimage()**函数：

**程序 1：**
**原始图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Use flopimage() function 
$gmagick->flopimage();

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/92c531b4da931f4354114ef4f63c9672.png)

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
$gmagick->annotateimage ( $draw , 50 , 60, 54 , 'GeeksForGeeks');
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Use flopimage() function 
$gmagick->flopimage();

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/9ad31a8c70b6eabc76a324dfd468d939.png)

**引用：**[http://php.net/manual/en/gmagick.flopimage.php](http://php.net/manual/en/gmagick.flopimage.php)