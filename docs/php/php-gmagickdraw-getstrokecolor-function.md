# PHP|GmagickDraw getstrokecolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getstrokecolor-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getstrokecolor-function/)

**GmagickDraw：：getstrokecolor()函数**是 PHP 中的一个内置函数，用于获取用于描边对象轮廓的颜色。

**语法：**

```php
*ImagickPixel* GmagickDraw::getstrokecolor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含颜色的 GmagickPixel 值。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：getstrokecolor()函数**：

**程序 1：**

```php
<?php  

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Get the stroke color 
$strokeColor = $draw->getstrokecolor()->getcolor(); 
echo $strokeColor; 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
rgb(0, 0, 0)
```

**程序 2：**

```php
<?php  

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Set the stroke color
$draw->setstrokecolor('#4a76bd');

// Get the stroke color 
$strokeColor = $draw->getstrokecolor()->getcolor(); 
echo $strokeColor; 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
rgb(19018, 30326, 48573)
```

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 3：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the color of stroke
$draw->setStrokeColor('red');

// Set the width of stroke
$draw->setstrokewidth(1);

// Set the font size
$draw->setFontSize(20);

// Get the stroke color
$strokecolor = $draw->getstrokecolor()->getcolor();

// Annotate a text
$draw->annotate(50, 100,
    'The stroke color here is ' . $strokecolor);

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/527b71d372cc49c732e4edb718ab0f7f.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.getstrokecolor.php](https://www.php.net/manual/en/gmagickdraw.getstrokecolor.php)