# PHP|GmagickDraw getstrokewidth()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getstrokewidth-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getstrokewidth-function/)

Gmagick：：getstrokewidth()函数是 PHP 中的一个内置函数，用于返回用于绘制对象轮廓的笔划宽度。

**语法：**

```
*public* GmagickDraw::getstrokewidth( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回描述笔划宽度的双精度。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的*Gmagick：：getstrokewidth()*函数：

**程序：**

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
$gmagick->drawImage($draw); 

// Using getstrokewidth() function

print_r($draw->getstrokewidth());

?> 
```

发帖主题：Re：Колибри0.7.0

```
7
```

**引用：**[http://php.net/manual/en/gmagickdraw.getstrokewidth.php](http://php.net/manual/en/gmagickdraw.getstrokewidth.php)