# PHP|GmagickDraw 椭圆()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-ellipse-function/](https://www.geeksforgeeks.org/php-gmagickdraw-ellipse-function/)

**GmagickDraw：：Ellipse()函数**是 PHP 中的一个内置函数，用于在图像上绘制椭圆。

**语法：**

```php
*GmagickDraw* GmagickDraw::ellipse( *float* $ox, 
*float* $oy, *float* $rx, *float* $ry, 
*float* $start, *float* $end )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$ox：**它指定椭圆的 x 坐标。
*   **$oy：**它指定椭圆的 y 坐标。
*   **$rx：**它指定椭圆的 x 半径。
*   **$ry：**它指定椭圆的 y 半径。
*   **$start：**它指定椭圆的起点。
*   **$end：**它指定椭圆的终点。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序说明了 PHP 中的**GmagickDraw：：Ellipse()函数**：
**程序 1(简单省略号)：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
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

// Draw a ellipse 
$draw->ellipse(125, 70, 100, 50, 0, 360); 

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/e40788f8cebeb9d7dc8ce7bc4b8dc805.png)

**程序 2(划线省略号)：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Function to draw rectangle
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('blue');

// Set the stroke color
$draw->setstrokecolor('green');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw a ellipse 
$draw->ellipse(225, 70, 150, 50, 0, 360); 

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/d8e803f22c0cbbe4fa405106721c8390.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.ellipse.php](https://www.php.net/manual/en/gmagickdraw.ellipse.php)