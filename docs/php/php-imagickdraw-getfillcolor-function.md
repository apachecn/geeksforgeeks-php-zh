# PHP|ImagickDraw getFillColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfillcolor-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfillcolor-function/)

**ImagickDraw：：getFillColor()函数**是 PHP 中的一个内置函数，用于获取用于绘制填充对象的填充颜色。

**语法：**

```
*ImagickPixel* ImagickDraw::getFillColor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含填充颜色的 ImagickPixel 值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getFillColor()函数**：

**程序 1：**

```
<?php
// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the Fill Color
$colorPixel = $draw->getFillColor();

// Convert ImagickPixel into string
$color = $colorPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.0

```
srgb(0, 0, 0) // which is black the default color.
```

**程序 2：**

```
<?php
// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the Fill Color
$draw->setFillColor('purple');

// Get the Fill Color
$colorPixel = $draw->getFillColor();

// Convert ImagickPixel into string
$color = $colorPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.0

```
srgb(128, 0, 128)
```

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('cyan');

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotation(50, 100, 'The fill color here is ' 
               . $draw->getFillColor()->getColorAsString());

// Set the fill color
$draw->setFillColor('red');

// Annotate a text
$draw->annotation(50, 200, 'The fill color here is ' 
               . $draw->getFillColor()->getColorAsString());

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/67aa71c909bf6beb063e132c93b8a5d8.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getfillcolor.php](https://www.php.net/manual/en/imagickdraw.getfillcolor.php)