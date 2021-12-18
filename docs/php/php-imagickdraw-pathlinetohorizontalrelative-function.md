# PHP|ImagickDraw pathLineToHorizontalRelative()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathlinetohorizontalrelative-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathlinetohorizontalrelative-function/)

**ImagickDraw：：pathLineToHorizontalRelative()函数**是 PHP 中的内置函数，用于使用相对坐标绘制从当前点到目标点的水平线路径。 然后，目标点将成为新的当前点。

**语法：**

```
*bool* ImagickDraw::pathLineToHorizontalRelative( *float* $x )
```

**参数：**此函数接受保存 x 坐标的单个参数**$x**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给定的程序说明了 PHP：
**程序 1：**中的**ImagickDraw：：pathLineToHorizontalRelative()函数**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('Green');

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw line using pathLineToHorizontalRelative
$draw->pathStart();
$draw->pathMoveToRelative(0, 100);
$draw->pathLineToHorizontalRelative(1000);
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
![](img/c0010d6748803bc56ddd21fc18bf48c6.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$color = ['blue', 'red', 'green', 'yellow', 'orange', 'brown', 'pink'];

// Set the stroke width
$draw->setStrokeWidth(5);

// Draw lines
for ($x = 0; $x < 7; $x++) {
    $draw->setStrokeColor($color[$x]);
    $draw->pathStart();
    $draw->pathMoveToRelative(0, $x * 40);
    $draw->pathLineToHorizontalRelative(800);
    $draw->pathFinish();

}

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/6e8208311420b258903b414ae740af73.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathlinetohorizontalrelative.php](https://www.php.net/manual/en/imagickdraw.pathlinetohorizontalrelative.php)