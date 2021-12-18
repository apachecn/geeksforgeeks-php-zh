# PHP|ImagickDraw pathStart()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathstart-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathstart-function/)

**ImagickDraw：：pathStart()函数**是 PHP 中的一个内置函数，用于声明路径图纸列表的开始。 稍后，使用*pathFinish()*函数来终止该列表。

**语法：**

```
*bool* ImagickDraw::pathStart( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**ImagickDraw：：pathStart()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create a image on Imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke width
$draw->setStrokeWidth(10);

$draw->setFillColor('green');

// Start the path
$draw->pathStart();

// Draw a pattern
$draw->pathMoveToRelative(400, 200);
$draw->pathLineToAbsolute(400, 100);
$draw->pathLineToAbsolute(300, 200);
$draw->pathLineToAbsolute(300, 100);

// End the path
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
![](img/3f048d62abf7435758f52ca252ffa8d3.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke width
$draw->setStrokeWidth(10);

// Set the stroke color
$draw->setStrokeColor('red');

// Set the fill color
$draw->setFillColor('white');

// Start the path
$draw->pathStart();
$x = 1;

// Draw a pattern
while ($x < 10) {
    $draw->pathMoveToAbsolute($x * 100, 0);
    $draw->pathLineToHorizontalAbsolute($x * 100);
    $draw->pathMoveToAbsolute(0, $x * 100);
    $x++;
}

$draw->pathclose();

// End the path
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
![](img/75f160962e29a579f333b993b3f772f4.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathstart.php](https://www.php.net/manual/en/imagickdraw.pathstart.php)