# PHP|ImagickDraw pathCurveToSmoothRelative()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathcurvetosmoothrelative-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathcurvetosmoothrelative-function/)

**ImagickDraw：：pathCurveToSmoothRelative()函数**是 PHP 中的一个内置函数，用于使用相对坐标绘制从当前点到(x，y)的三次贝塞尔曲线。

**语法：**

```
*bool* ImagickDraw::pathCurveToSmoothRelative( *float* $x2, *float* $y2, *float* $x, *float* $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$x2：**它指定第二个控制点的 x 坐标。
*   **$y2：**它指定第二个控制点的 y 坐标。
*   **$x：**它指定终点的 x 坐标。
*   **$y：**它指定终点的 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：pathCurveToSmoothRelative()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'skyblue');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('skyblue');

// Set the stroke color
$draw->setStrokeColor('black');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw a painting
$draw->pathStart();
$draw->pathMoveToRelative(335, 70);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathMoveToRelative(50, 50);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathMoveToRelative(-500, 0);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathCurveToSmoothRelative(50, -50, 60, 20);
$draw->pathFinish();

// Set the fill color
$draw->setFillColor('yellow');

// Draw a circle
$draw->circle(20, 20, 100, 20);

// Set the stroke width
$draw->setStrokeWidth(1);

// Set the fond size
$draw->setFontSize(40);

// Set the fill color
$draw->setFillColor('yellow');

// Annotate the text
$draw->annotation(500, 40, 'Summer Vibes');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/096e3377b252d1a3705607e6eed6f5e4.png)

**程序 2：**

```
<?php
// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'cyan');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$draw->setFillColor('purple');

// Set the stroke color
$draw->setStrokeColor('blue');

// Set the stroke width
$draw->setStrokeWidth(15);

// Draw curves to Quadratic Bezier Relative (with pathClose())
$draw->pathStart();
$draw->pathCurveToSmoothRelative(-200, 250, 1900, 1250);
$draw->pathClose();
$draw->pathFinish();

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/ca0707b35501eabe22aa4ac62ba1e336.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathcurvetosmoothrelative.php](https://www.php.net/manual/en/imagickdraw.pathcurvetosmoothrelative.php)