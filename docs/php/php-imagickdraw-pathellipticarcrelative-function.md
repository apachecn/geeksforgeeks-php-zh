# PHP|ImagickDraw 路径 EllipticArcRelative()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathellipticarcrelative-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathellipticarcrelative-function/)

**ImagickDraw：：pathEllipticArcRelative()函数**是 PHP 中的一个内置函数，用于使用相对坐标绘制从当前点到(x，y)的椭圆弧。

**语法：**

```php
*bool* ImagickDraw::pathEllipticArcRelative( *float* $rx, *float* $ry,
         *float* $x_axis_rotation, *bool* $large_arc_flag, *bool* $sweep_flag, *float* $x )
```

**参数：**此函数接受上述 7 个参数，如下所述：

*   **$rx：**它指定 x 半径。
*   **$ry：**它指定 y 半径
*   **$x_AXIS_ROTATION：**它指定 x 轴旋转
*   **$LARGE_ARC_FLAG：**它指定是否绘制较大的可用圆弧。
*   **$Sweep_flag：**它指定是否绘制与时钟方向旋转匹配的圆弧。
*   **$x：**它指定 x 坐标。
*   **$y：**它指定 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**ImagickDraw：：pathEllipticArcRelative()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#7441e0');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$draw->setFillColor('#2fceeb');

// Set the stroke color
$draw->setStrokeColor('#c27230');

// Set the stroke width
$draw->setStrokeWidth(15);

// Draw elliptic arc
$draw->pathStart();
$draw->pathEllipticArcRelative(120, 9250,
               210, false, true, 300, 400);
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
![](img/ab2cf4d9a910d6768b66997ec18f0098.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#7441e0');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$draw->setFillColor('#2fceeb');

// Set the stroke color
$draw->setStrokeColor('#c27230');

// Set the stroke width
$draw->setStrokeWidth(15);

// Draw elliptic arc
$draw->pathStart();
$draw->pathEllipticArcRelative(120,
         50, 10, true, true, 300, 400);
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
![](img/fe409b71b0ffa3f371a2185641b6dc58.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathellipticarcrelative.php](https://www.php.net/manual/en/imagickdraw.pathellipticarcrelative.php)