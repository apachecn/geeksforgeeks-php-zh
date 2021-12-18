# PHP|ImagickDraw setStrokeLineCap()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setstrokelinecap-function/](https://www.geeksforgeeks.org/php-imagickdraw-setstrokelinecap-function/)

**ImagickDraw：：setStrokeLineCap()函数**是 PHP 中的一个内置函数，用于设置在打开的子路径被描边时要使用的形状。

**语法：**

```
*bool* ImagickDraw::setStrokeLineCap( *int* $linecap )
```

**参数：**此函数接受单个参数**$linecap**，该参数保存与[LINECAP 常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.linecap-undefined)之一相对应的整数值。

LINECAP 常量列表如下：

*   Imagick：：LINECAP_UNDEFINED(0)
*   Imagick：：LINECAP_BUT(1)
*   Imagick：：LINECAP_ROUND(2)
*   Imagick：：LINECAP_Square(3)

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickDraw：：setStrokeLineCap()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke line cap
$draw->setStrokeLineCap(2);

// Get the stroke line cap
$lineCap = $draw->getStrokeLineCap();
echo $lineCap;
?>
```

发帖主题：Re：Колибри0.7.0

```
2 // Which corresponds to imagick::LINECAP_ROUND
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'grey');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the color of stroke
$draw->setStrokeColor('red');

// Set stroke width
$draw->setStrokeWidth(3);

// Set the font size
$draw->setFontSize(25);

 // Set the stroke dash array
$draw->setStrokeDashArray([20]);

// Set the stroke line cap
$draw->setStrokeLineCap(3);

// Draw a circle
$draw->circle(250, 150, 330, 130);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/14eddbb622b53fceaeef32d6d99c3ef6.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setstrokelinecap.php](https://www.php.net/manual/en/imagickdraw.setstrokelinecap.php)