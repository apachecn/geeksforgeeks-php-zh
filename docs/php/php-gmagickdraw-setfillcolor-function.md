# PHP|GmagickDraw setfulcolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfillcolor-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfillcolor-function/)

**GmagickDraw：：setficolor()函数**是 PHP 中的一个内置函数，用于设置绘制时使用的填充颜色。

**语法：**

```php
*GmagickDraw* GmagickDraw::setfillcolor( *mixed* $color )
```

**参数：**此函数接受单个参数**$color**，该参数用于保存像素颜色值。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**GmagickDraw：：setfulcolor()函数**：

**程序 1：**带填充颜色的矩形。

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(5, 10, 660, 100);

// Set the fill color
$draw->setfillcolor('green');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/0931a06c0d18bd585fab1dcdf267b6b1.png)

**程序 2：**带填充颜色的文本。

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-100, -1000, 800, 400);

// Set the fill color
$draw->setfontsize(90);

// Set the stroke color
$draw->setstrokecolor('red');

// Set the fill color for background rectangle and text
$draw->setfillcolor('blue');

// Create a rectangle
$draw->annotate(20, 110, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/58b5d963a515c2bab9f86ef8c6fbeb46.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.setfillcolor.php](https://www.php.net/manual/en/gmagickdraw.setfillcolor.php)