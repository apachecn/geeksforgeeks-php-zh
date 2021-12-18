# PHP|Gmagick spreadimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-spreadimage-function/](https://www.geeksforgeeks.org/php-gmagick-spreadimage-function/)

**gmagick：：spreadimage()**函数是 PHP 中的一个内置函数，用于随机替换变量定义的块中的每个像素。

**语法：**

```php
*Gmagick* Gmagick::spreadimage( $radius )
```

*
**参数：**此函数接受单个参数*$Radius*，该参数选择此范围附近的随机像素。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：spreadimage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// spread the image. 
$gmagick->spreadimage(10); 

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?>
```

**输出：**
![](img/c3edb477958d773b83de2a324afdcb12.png)

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

// Spread the image
$gmagick->spreadimage(25);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/5c7a7cafd93722101c1d66e81f5d302b.png)

**引用：**[http://php.net/manual/en/gmagick.spreadimage.php](http://php.net/manual/en/gmagick.spreadimage.php)