# PHP|ImagickDraw pathLineToRelative()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathlinetorelative-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathlinetorelative-function/)

**ImagickDraw：：pathLineToRelative()函数**是 PHP 中的一个内置函数，用于使用相对坐标绘制从当前点到给定坐标的直线路径。 然后，该坐标将成为新的当前点。 初始点可以使用*pathMoveToRelative()*函数设置。

**语法：**

```
*bool* ImagickDraw::pathLineToRelative( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定起始 x 坐标。
*   **$y：**它指定起始 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**ImagickDraw：：pathLineToRelative()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('black');

// Create a path
$draw->pathStart();

// Draw a line
// Start coordinates of line
$draw->pathMoveToRelative(350, 50);

// End coordinates of line
$draw->pathLineToRelative(50, 150);

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
![](img/8e2b9322e39ebb3a125c13306bfaff99.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('yellow');

// Set the stroke color
$draw->setStrokeColor('black');

// Set the stroke width
$draw->setStrokeWidth(1);

// Create a path
$draw->pathStart();

// Draw a star
$draw->pathMoveToRelative(350, 20); 
$draw->pathLineToRelative(40, 60); 
$draw->pathLineToRelative(80, 20); 
$draw->pathLineToRelative(-80, 30); 
$draw->pathLineToRelative(30, 60); 
$draw->pathLineToRelative(-50, -20); 
$draw->pathLineToRelative(-50, 40); 
$draw->pathLineToRelative(10, -70); 
$draw->pathLineToRelative(-50, -10); 
$draw->pathLineToRelative(50, -30); 
$draw->pathLineToRelative(20, -80); 

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
![](img/16a30321265d8904e6e317123cc6c971.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathlinetorelative.php](https://www.php.net/manual/en/imagickdraw.pathlinetorelative.php)