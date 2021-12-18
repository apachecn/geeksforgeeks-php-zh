# PHP|ImagickDraw getStrokeColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getstrokecolor-function/](https://www.geeksforgeeks.org/php-imagickdraw-getstrokecolor-function/)

**ImagickDraw：：getStrokeColor()函数**是 PHP 中的一个内置函数，用于获取用于描边对象轮廓的颜色。

**语法：**

```php
*ImagickPixel* ImagickDraw::getStrokeColor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含笔划颜色的 ImagickPixel。

下面的程序说明了 PHP 中的**ImagickDraw：：getStrokeColor()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the stroke color
$strokeColor = $draw->getStrokeColor()->getColorAsString();
echo $strokeColor;
?>
```

发帖主题：Re：Колибри0.7.0

```php
srgba(255, 255, 255, 0)
```

**程序 2：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('grey');

// Get the stroke color
$strokeColor = $draw->getStrokeColor()->getColorAsString();
echo $strokeColor;
?>
```

发帖主题：Re：Колибри0.7.0

```php
srgb(190, 190, 190)
```

**程序 3：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('black');

// Set the width of stroke
$draw->setStrokeWidth(1);

// Set the color of stroke
$draw->setStrokeColor('red');

// Set the font size
$draw->setFontSize(40);

// Get the stroke color
$strokecolor = $draw->getStrokeColor()->getColorAsString();

// Annotate a text
$draw->annotation(50, 100, 
    'The stroke color here is ' . $strokecolor);

// Set the color of stroke
$draw->setStrokeColor('green');

// Get the stroke color
$strokecolor = $draw->getStrokeColor()->getColorAsString();

// Annotate a text
$draw->annotation(50, 200,
    'The stroke color here is ' . $strokecolor);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3b5291f70705b4efff27ac65dbb8d08d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getstrokecolor.php](https://www.php.net/manual/en/imagickdraw.getstrokecolor.php)