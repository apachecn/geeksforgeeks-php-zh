# PHP|ImagickDraw setStrokeDashOffset()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setstrokedashoffset-function/](https://www.geeksforgeeks.org/php-imagickdraw-setstrokedashoffset-function/)

**ImagickDraw：：setStrokeDashOffset()函数**是 PHP 中的一个内置函数，用于设置划线模式中的偏移量以开始划线。

**语法：**

```
*bool* ImagickDraw::setStrokeDashOffset( *float* $dash_offset )
```

**参数：**此函数接受保存破折号偏移量的单个参数**$dash_Offset**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickDraw：：setStrokeDashOffset()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke dash offset
$draw->setStrokeDashOffset(5);

// Get the stroke dash offset
$offset = $draw->getStrokeDashOffset();
echo $offset;
?>
```

发帖主题：Re：Колибри0.7.0

```
5
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('black');

// Set the color of stroke
$draw->setStrokeColor('white');

 // Set the stroke dash array
$draw->setStrokeDashArray([15, 5, 15]);

// Set the stroke dash offset
$draw->setStrokeDashOffset(20);

// Draw a circle using ellipse function
$draw->ellipse(400, 100, 70, 70, 60, 900);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3a1eb5f232e3bc0eb4fdf7f7a1a7a33c.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setstrokedashoffset.php](https://www.php.net/manual/en/imagickdraw.setstrokedashoffset.php)