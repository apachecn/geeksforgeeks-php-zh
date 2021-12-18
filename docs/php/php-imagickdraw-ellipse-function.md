# PHP|ImagickDraw 椭圆()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-ellipse-function/](https://www.geeksforgeeks.org/php-imagickdraw-ellipse-function/)

**ImagickDraw：：Ellipse()函数**是 PHP 中的内置函数，用于在图像上绘制椭圆。

**语法：**

```
*bool* ImagickDraw::ellipse( *float* $ox, *float* $oy, 
*float* $rx, *float* $ry, *float* $start, *float* $end )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$ox：**它指定椭圆的 x 坐标。
*   **$oy：**它指定椭圆的 y 坐标。
*   **$rx：**它指定椭圆的 x 半径。
*   **$ry：**它指定椭圆的 y 半径。
*   **$start：**它指定椭圆的起点。
*   **$end：**它指定椭圆的终点。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：Ellipse()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'purple');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Draw a ellipse
$draw->ellipse(125, 70, 100, 50, 0, 360);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d80e1f7116d2d9b87ec95c6048bb245a.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'brown');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Draw a black ellipse
$draw->ellipse(400, 120, 200, 100, 0, 360);

// Set the FillColor to green
$draw->setFillColor('green');

// Draw a green ellipse
$draw->ellipse(400, 120, 150, 90, 0, 360);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/eb570859e207f17542cde4ad8538359d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.ellipse.php](https://www.php.net/manual/en/imagickdraw.ellipse.php)