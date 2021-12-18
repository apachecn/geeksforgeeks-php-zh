# PHP|ImagickDraw pathLineToHorizontalAbsolute()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathlinetohorizontalabsolute-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathlinetohorizontalabsolute-function/)

**ImagickDraw：：pathLineToHorizontalAbsolute()函数**是 PHP 中的内置函数，用于使用绝对坐标绘制从当前点到目标点的水平线路径。 然后，目标点将成为新的当前点。 也可以使用*pathMoveToRelative()*函数设置当前点。

**语法：**

```
*bool* ImagickDraw::pathLineToHorizontalAbsolute( *float* $x )
```

**参数：**此函数接受保存 x 坐标的单个参数**$x**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：pathLineToHorizontalAbsolute()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('blue');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw line using pathLineToHorizontalAbsolute
$draw->pathStart();
$draw->pathMoveToRelative(0, 100);
$draw->pathLineToHorizontalAbsolute(1000);
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
![](img/f6e04f913689e97121be824ef821aec3.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('black');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw lines
$draw->pathStart();
for($x = 0; $x < 15; $x++) {
    $draw->pathMoveToRelative(0, 20);
    if($x % 2) {
        $draw->pathLineToHorizontalAbsolute(0);
    } else {
        $draw->pathLineToHorizontalAbsolute(1000);
    }
}

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
![](img/4aa0292e8d8d0db12c3f99959dff8ce8.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathlinetohorizontalabsolute.php](https://www.php.net/manual/en/imagickdraw.pathlinetohorizontalabsolute.php)