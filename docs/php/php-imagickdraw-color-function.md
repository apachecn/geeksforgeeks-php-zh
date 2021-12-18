# PHP|ImagickDraw color()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-color-function/](https://www.geeksforgeeks.org/php-imagickdraw-color-function/)

**ImagickDraw：：color()函数**是 PHP 中的一个内置函数，用于使用当前填充颜色、从指定位置开始并使用指定的绘制方法在图像上绘制颜色。

**语法：**

```php
*bool* ImagickDraw::color( *float* $x, *float* $y, *int* $paintMethod )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$x：**它指定绘画的 x 坐标。
*   **$y：**它指定绘画的 y 坐标。
*   **$aint tMethod：**它指定与[绘制常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.paint-point)之一相对应的整数。
    油漆常量列表如下：
    *   Imagick：：Paint_point(1)
    *   Imagick：：Paint_Replace(2)
    *   Imagick：：Paint_FLOODFILL(3)
    *   Imagick：：Paint_FILLTOBORDER(4)
    *   Imagick：：Paint_Reset(5)

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：color()函数**：

**程序 1：**

```php
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$x = 0;
while ($x < 900) {
    // Draw lines using imagick::PAINT_POINT
    $draw->color($x, 0, 1);
    $draw->color($x, 30, 1);
    $draw->color($x, 60, 1);
    $draw->color($x, 90, 1);
    $draw->color($x, 120, 1);
    $draw->color($x, 150, 1);
    $draw->color($x, 180, 1);
    $draw->color($x, 210, 1);
    $draw->color($x, 240, 1);
    $x++;
}

//  Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/9e4ee39714db74fc5839f7643b62ea26.png)

**程序 2：**

```php
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('green');

// Color the image using Imagick::PAINTFILL
$draw->color(1, 1, Imagick::PAINT_FLOODFILL);

//  Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/2c5bc122ad25c5bb2c86895db295b365.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.color.php](https://www.php.net/manual/en/imagickdraw.color.php)