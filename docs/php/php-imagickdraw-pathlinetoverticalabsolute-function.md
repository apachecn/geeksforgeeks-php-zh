# PHP|ImagickDraw pathLineToVerticalAbsolute()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pathlinetoverticalabsolute-function/](https://www.geeksforgeeks.org/php-imagickdraw-pathlinetoverticalabsolute-function/)

**ImagickDraw：：pathLineToVerticalAbsolute()函数**是 PHP 中的一个内置函数，用于使用绝对坐标绘制从当前点到目标点的垂直线路径。 然后，目标点将成为新的当前点。

**语法：**

```php
*bool* ImagickDraw::pathLineToVerticalAbsolute( *float* $y )
```

**参数：**此函数接受保存 y 坐标的单个参数**$y**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：pathLineToVerticalAbsolute()函数**：

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
$draw->setStrokeWidth(5);

// Draw a verticle line
$draw->pathStart();
$draw->pathMoveToRelative(400, 0);
$draw->pathLineToVerticalAbsolute(800);
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
![](img/c924690e58984d65148382216bc2453b.png)

**程序 2：**

```php
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
    $draw->pathMoveToRelative(50, 0);
    if($x % 2) {
        $draw->pathLineToVerticalAbsolute(0);
    } else {
        $draw->pathLineToVerticalAbsolute(1000);
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
![](img/f57bd04cfbc65ac6784f913062f2e12d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pathlinetoverticalabsolute.php](https://www.php.net/manual/en/imagickdraw.pathlinetoverticalabsolute.php)