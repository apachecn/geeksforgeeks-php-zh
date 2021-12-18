# PHP|ImagickDraw line()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-line-function/](https://www.geeksforgeeks.org/php-imagickdraw-line-function/)

**ImagickDraw：：Line()**函数是 PHP 的 Imagick 库中的内置函数，用于绘制直线。 此函数使用当前笔触颜色、笔触不透明度和笔触宽度绘制线条。

**语法：**

```php
*bool* ImagickDraw::line( $sx, $sy, $ex, $ey )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$sx：**此参数取起始 x 坐标的值。
*   **$sy：**此参数采用起始 y 坐标的值。
*   **$ex：**此参数取结束 x 坐标的值。
*   **$ey：**此参数采用结束 y 坐标的值。

**返回值：**如果成功，此函数返回 TRUE。
下面的程序说明 PHP：
**程序：**中的**ImagickDraw：：Line()**函数

## PHP

```php
<?php

// Create an Imagick object
$draw = new \ImagickDraw();

// Function to fill color
$draw->setFillColor('red');

// Function to draw line
$draw->line(10, 30, 180, 200);

// Create Imagick object
$imagick = new \Imagick();

// Create new image of given size
$imagick->newImage(300, 300, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Function to draw the image
$imagick->drawImage($draw);

header("Content-Type: image/png");

// Display the output image   
echo $imagick->getImageBlob();
?>
```