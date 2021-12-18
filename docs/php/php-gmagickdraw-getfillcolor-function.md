# PHP|GmagickDraw getfitcolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getfillcolor-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getfillcolor-function/)

**GmagickDraw：：getfitcolor()函数**是 PHP 中的一个内置函数，用于获取用于绘制填充对象的填充颜色。

**语法：**

```php
*GmagickPixel* GmagickDraw::getfillcolor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回用于绘制填充对象的 GmagickPixel 填充颜色。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：getfitcolor()函数**：

**程序-1：**

```php
<?php 
// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Set the fill color
$draw->setfillcolor('blue');

// Get the fill color 
$colorPixel = $draw->getfillcolor(); 
$color = $colorPixel->getcolor();
echo $color; 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
rgb(0, 0, 65535)
```

**程序-2：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotate(50, 50, 'The fill color here is ' . $draw->getFillColor()->getcolor());

// Set the fill color
$draw->setFillColor('red');

// Annotate a text
$draw->annotate(50, 100, 'The fill color here is ' . $draw->getFillColor()->getcolor());

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/8a47b80dd05858caa3906bbcea41f658.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.getfillcolor.php](https://www.php.net/manual/en/gmagickdraw.getfillcolor.php)