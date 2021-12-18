# PHP|GmagickDraw arc()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-arc-function/](https://www.geeksforgeeks.org/php-gmagickdraw-arc-function/)

**GmagickDraw：：arcc()函数**是 PHP 中的一个内置函数，用于在图像上绘制落在指定边界矩形内的圆弧。

**语法：**↔

```php
*GmagickDraw* GmagickDraw::arc( *float* $sx, *float* $sy,
              *float* $ex, *float* $ey, *float* $sd, *float* $ed )
```

***参数：**此函数接受上述六个参数，如下所述：

*   **$sx：**它指定矩形的起始 x 坐标。
*   **$sy：**它指定矩形的起始 y 坐标。
*   **$ex：**它指定矩形的终点 x 坐标。
*   **$ey：**它指定矩形的结束 y 坐标。
*   **$SD：**它指定旋转的起始度。
*   **$ed：**它指定旋转的结束度数。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：arcc()函数**：

**使用的图像：**![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(从头绘制圆弧)：**

## PHP

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the stroke color
$draw->setstrokecolor('black');

// Set the stroke width
$draw->setStrokeWidth(5); 

// Mark a arc
$draw->arc(60, -60, 460, 170, 0, 200);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/7beed7bc4431074e52d2851b7ea0bca0.png)

**程序 2(在图像上绘制圆弧)：**

## PHP

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the fill color
$draw->setFillColor('red');

// Set the stroke color
$draw->setstrokecolor('green');

// Set the stroke width
$draw->setStrokeWidth(5); 

// Mark a arc
$draw->arc(160, -60, 360, 170, 50, 200);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/4239d36c043c1e8c631820362f4fe1d2.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.arc.php](https://www.php.net/manual/en/gmagickdraw.arc.php)