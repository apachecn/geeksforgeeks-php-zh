# PHP|GmagickDraw setstrokeopacity()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setstrokeopacity-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setstrokeopacity-function/)

GmagickDraw：：setstrokeopacity()函数是 PHP 中的一个内置函数，用于指定描边对象轮廓的不透明度。 不透明度的值介于 0 和 1 之间。

**语法：**

```php
*public* GmagickDraw::setstrokeopacity( $stroke_opacity ) : GmagickDraw
```

**参数：**此函数接受单个参数*$kes_opacity*，该参数用于将笔划不透明度的值保存为浮点类型。
**返回值：**此函数成功时返回 GmagickDraw 对象。
以下程序说明 PHP：
**程序 1：**中的 GmagickDraw：：setstrokeopacity()函数

## PHP

```php
<?php

// require_once('path/vendor/autoload.php');

// Create an GmagickDraw object to draw into.
$draw = new \GmagickDraw();

// Set the stroke color
$draw->setStrokeColor('Green');

// Set the filled color
$draw->setFillColor('Red');

// Set the stroke opacity
$draw->setStrokeOpacity(0.5);

// Set the stroke width
$draw->setStrokeWidth(9);

// Draw the rectangle
$draw->rectangle(40, 30, 200, 260);

// Create new gmagick object
$image = new \Gmagick();

// Create new image of given size
$image->newImage(240, 300, 'White');

// Set the image format
$image->setImageFormat("png");

// Draw the image
$image->drawImage($draw);

header("Content-Type: image/png");

// Display the output image
echo $image->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![setstrokeopacity](img/f37935f20d01594f418233454f09f8b2.png)

**程序 2：**

## PHP

```php
<?php

// require_once('path/vendor/autoload.php');

// Create an GmagickDraw object to draw into.
$draw = new \GmagickDraw();

// Set the Stroke Color
$draw->setStrokeColor('Black');

// Set the Stroke Opacity
$draw->setStrokeOpacity(0.6);

// Set the Stroke Width
$draw->setStrokeWidth(4);

//Set the filled color
$draw->setFillColor('lightgreen');
$points = [
        ['x' => 50 * 6, 'y' => 10 * 5],
        ['x' => 20 * 7, 'y' => 30 * 5],
        ['x' => 60 * 8, 'y' => 50 * 5],
        ['x' => 70 * 3, 'y' => 15 * 5],
    ];

// Draw the polygon
$draw->polygon($points);

// Create new Gmagick object
$image = new \Gmagick();

// Set the image dimensions
$image->newImage(500, 300, 'white');

// Set the image format
$image->setImageFormat("png");

// Draw the image
$image->drawImage($draw);

header("Content-Type: image/png");

// Display the image
echo $image->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![setstrokeopacity](img/f62a1f107572d3fa943712ba6e80b305.png)

**引用：**[http://php.net/manual/en/gmagickdraw.setstrokeopacity.php](http://php.net/manual/en/gmagickdraw.setstrokeopacity.php)