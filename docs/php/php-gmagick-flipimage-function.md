# PHP|Gmagick flipimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-flipimage-function/](https://www.geeksforgeeks.org/php-gmagick-flipimage-function/)

**Gmagick：：flipimage()**函数是 PHP 中的一个内置函数，用于翻转图像。 此函数通过沿 x 轴反射像素来创建镜像图像。

**语法：**

```
*Gmagick* Gmagick::flipimage( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回翻转的 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：flipimage()**函数：

**程序 1：**
**原始图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Use flipimage() function 
$gmagick->flipimage();

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/02aaa2a3a075cba9ffb629c1256ff2e2.png)

**程序 2：**

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
$gmagick->annotateimage ( $draw, 50, 60, 54, 'GeeksForGeeks');
$gmagick->drawImage($draw); 

// Use flipimage() function 
$gmagick->flipimage();

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/0e21b588b07c2e9100726225b2b8866f.png)

**引用：**[http://php.net/manual/en/gmagick.flipimage.php](http://php.net/manual/en/gmagick.flipimage.php)