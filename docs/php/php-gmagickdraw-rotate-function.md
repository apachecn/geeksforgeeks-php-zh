# PHP|GmagickDraw Rotate()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-rotate-function/](https://www.geeksforgeeks.org/php-gmagickdraw-rotate-function/)

**GmagickDraw：：Rotate()函数**是 PHP 中的一个内置函数，用于将指定的旋转应用于当前坐标空间。

**语法：**

```php
*GmagickDraw* GmagickDraw::rotate( *array* $coordinates_array )
```

**参数：**此函数接受单个参数**$coides_array**，该参数用于保存旋转度的值。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

**画布区域使用的图像：**。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序说明了 PHP 中的**GmagickDraw：：Rotate()函数**：

**程序 1：**在本例中，我们将旋转矩形。

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-100, -1000, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the stroke color
$draw->setstrokecolor('blue');

// Rotate by 4 degrees
$draw->rotate(4);

// Set the stroke width
$draw->setStrokeWidth(5);

// Create a rectangle
$draw->rectangle(100, 20, 400, 100); 

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/21bdb50a5a1f63a0cd18e4204dea4946.png)

**程序 2：**在本例中，我们将旋转文本。

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-100, -1000, 800, 400);

// Set the font size
$draw->setfontsize(25);

// Set the stroke color
$draw->setstrokecolor('blue');

// Rotate by 40
$draw->rotate(40);

// Annotate a text
$draw->annotate(20, -50, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/d72429f3bbb50a000cb583fb273fa3f0.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.rotate.php](https://www.php.net/manual/en/gmagickdraw.rotate.php)