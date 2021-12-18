# PHP|GmagickDraw Bezier()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-bezier-function/](https://www.geeksforgeeks.org/php-gmagickdraw-bezier-function/)

**GmagickDraw：：Bezier()函数**是 PHP 中的内置函数，用于绘制 Bezier 曲线。

**语法：**

```php
*GmagickDraw* GmagickDraw::bezier( *array* $coordinate_array )
```

**参数：**此函数接受单个参数**$CODERATE_ARRAY**，该参数保存多维数组，该数组采用要绘制曲线的点。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。
**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**GmagickDraw：：Bezier()函数**：

**程序 1：**简单贝塞尔曲线

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Function to draw rectangle
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('#3D99D4');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw the curve
$draw->bezier([
    ['x' => 10, 'y' => 10],
    ['x' => 0, 'y' => 0],
    ['x' => 620, 'y' => 0],
    ['x' => 550, 'y' => 170],
]);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/113472e07f5f92c1ceeea9bb3078defa.png)

**程序 2：**带描边和填充的贝塞尔曲线

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Function to draw rectangle
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('yellow');

// Set the stroke color
$draw->setstrokecolor('purple');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw the curve
$draw->bezier([
    ['x' => 10, 'y' => 10],
    ['x' => 0, 'y' => 150],
    ['x' => 620, 'y' => 0],
    ['x' => 550, 'y' => 170],
]);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/d8998484d830390883c3821253634d87.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.bezier.php](https://www.php.net/manual/en/gmagickdraw.bezier.php)