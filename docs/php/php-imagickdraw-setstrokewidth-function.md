# PHP|ImagickDraw setStrokeWidth()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setstrokewidth-function/](https://www.geeksforgeeks.org/php-imagickdraw-setstrokewidth-function/)

**ImagickDraw：：setStrokeWidth()**函数是 PHP 中的内置函数，用于设置用于绘制对象轮廓的笔划宽度。

**语法：**

```php
*bool* ImagickDraw::setStrokeWidth( $stroke_width )
```

**参数：**此函数接受单个参数*$kes_width*，该参数用于保存笔划宽度的值。 它是浮点型的值。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**ImagickDraw：：setStrokeWidth()函数**：

**程序 1：**

```php
<?php

// Create new Imagick object 
$draw = new \ImagickDraw();

// Set the stroke Color
$draw->setStrokeColor('Red');

// Set the image filled color 
$draw->setFillColor('Green');

// Set the Stroke Width
$draw->setStrokeWidth(7);

// Draw the Circle
$draw->circle(250, 250, 100, 150);

// Create new Imagick Object
$imagick = new \Imagick();

// Set the dimensions of image
$imagick->newImage(500, 500, 'White');

// Set the image format 
$imagick->setImageFormat("png");

// Draw the image 
$imagick->drawImage($draw);

header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![setStrokeWidth](img/b9d353806be03607ab208470060b190f.png)

**程序 2：**

```php
<?php
// Create new Imagick Object 
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('black');

// Set the image filled color 
$draw->setFillColor('lightgreen');

// Set the Stroke Width
$draw->setStrokeWidth(0);

// Draw the rectangle
$draw->rectangle(100, 100, 300, 300);

// Set Stroke Width
$draw->setStrokeWidth(15);

// Draw the rectangle
$draw->rectangle(400, 100, 600, 300);

// Create new Imagick Object 
$imagick = new \Imagick();

// Set the dimensions of image
$imagick->newImage(800, 500, 'White');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image 
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image 
echo $imagick->getImageBlob();
?>
```

**输出：**
![setStrokeWidth](img/bae3819f8178b4e3f6a9bbe6b678ea73.png)

**引用：**[http://php.net/manual/en/imagickdraw.setstrokewidth.php](http://php.net/manual/en/imagickdraw.setstrokewidth.php)