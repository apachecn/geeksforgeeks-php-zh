# PHP|GmagickDraw Polyline()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-polyline-function/](https://www.geeksforgeeks.org/php-gmagickdraw-polyline-function/)

**GmagickDraw：：Polyline()函数**是 PHP 中的一个内置函数，用于使用指定的坐标数组，使用当前笔划、笔划宽度和填充颜色或纹理绘制多段线。

**语法：**

```php
*GmagickDraw* GmagickDraw::polyline( *array* $coordinates_array )
```

**参数：**此函数接受单个参数**$cotalesarray**，该参数用于将点的坐标保存为数组。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

**使用的图像：**![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面的示例说明了 PHP 中的**GmagickDraw：：Polyline()函数**：

**程序 1：**在图像上绘制

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the fill color
$draw->setFillColor('#0E0E0E');

// Set the stroke color
$draw->setstrokecolor('green');

// Set the stroke width
$draw->setStrokeWidth(5);

// Create a polygonline
$draw->polyline([
    ['x' => 100, 'y' => 50],
    ['x' => 40, 'y' => 150],
    ['x' => 480, 'y' => 150],
    ['x' => 110, 'y' => 75],
]);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/257a50e09c51356d7453670ee52f333f.png)

**程序 2：**从头开始绘图

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the stroke color
$draw->setstrokecolor('red');

// Set the stroke width
$draw->setStrokeWidth(5);

// Create a polygonline
$draw->polyline([
    ['x' => 400, 'y' => 0],
    ['x' => 40, 'y' => 170],
    ['x' => 480, 'y' => 150],
    ['x' => 110, 'y' => 5],
]);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/6dbe026185e91dd6f47322307be203ee.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.polyline.php](https://www.php.net/manual/en/gmagickdraw.polyline.php)