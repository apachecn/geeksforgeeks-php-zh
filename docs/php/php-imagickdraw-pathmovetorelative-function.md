# PHP|ImagickDraw pathMoveToRelative()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathmovetorelative-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathmovetorelative-function/)

**ImagickDraw：：pathMoveToRelative()函数**是 PHP 中的一个内置函数，用于使用相对坐标在给定坐标处启动新的子路径。 然后，当前点将成为指定的坐标。 此函数用于在开始绘制任何内容之前设置初始坐标。

**语法：**

```php
*bool* ImagickDraw::pathMoveToRelative( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定 x 坐标。
*   **$y：**它指定 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：pathMoveToRelative()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke width
$draw->setStrokeWidth(30);

$draw->pathStart();

// Setting the stating point to (400, 100)
$draw->pathMoveToRelative(400, 100);

// Setting the end point to (500, 100)
$draw->pathLineToHorizontalAbsolute(500);
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
![](img/f565b71c7dd6199c9cdae2b0bf5d8649.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke width
$draw->setStrokeWidth(30);

$draw->setFillColor('red');

$draw->pathStart();

// Setting the stating point to (400, 100), draw a rectangle
$draw->pathMoveToRelative(400, 100);
$draw->pathLineToAbsolute(400, 200);
$draw->pathLineToAbsolute(300, 200);
$draw->pathLineToAbsolute(300, 100);

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
![](img/776f954dc3f76945f7ac19d26547283f.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathmovetorelative.php](https://www.php.net/manual/en/imagickdraw.pathmovetorelative.php)