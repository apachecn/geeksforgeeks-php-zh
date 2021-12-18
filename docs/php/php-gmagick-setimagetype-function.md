# PHP|Gmagick setimagetype()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagetype-function/](https://www.geeksforgeeks.org/php-gmagick-setimagetype-function/)

**gmagick：：setimagetype()函数**是 PHP 中的一个内置函数，用于设置图像类型。

**语法：**

```php
*Gmagick* Gmagick::setimagetype( *int* $imgType )
```

**参数：**此函数接受单个参数**$imgType**，该参数保存与[IMGTYPE 常量](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.imgtype-undefined)之一相对应的整数值。

下面列出了所有 IMGTYPE 常量：

*   Gmagick：：IMGTYPE_UNDEFINED(0)
*   Gmagick：：IMGTYPE_BILLEVEL(1)
*   Gmagick：：IMGTYPE_GRAYSCALE(2)
*   Gmagick：：IMGTYPE_GRAYSCALEMATTE(3)
*   Gmagick：：IMGTYPE_Palette(4)
*   GMAGICK：：IMGTYPE_PALETTEMATTE(5)
*   Gmagick：：IMGTYPE_TRUECOLOR(6)
*   Gmagick：：IMGTYPE_TRUECOLORMATTE(7)
*   Gmagick：：IMGTYPE_COLORSEPARATION(8)
*   Gmagick：：IMGTYPE_COLORSEPARATIONMATTE(9)
*   GMAGICK：：IMGTYPE_OPTIMIZE(10)

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimagetype()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image type
$gmagick->setimagetype(1);

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/3b4ed2dd1bdf825e0d4cf4cc0ad8bf12.png)

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image type
$gmagick->setimagetype(3);

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/f1e67d3f60d9039d4ee22ed4f68f909f.png)

**程序 3：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('red');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Set the image type
$gmagick->setimagetype(2);

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/b3c0a0797a8d2732bc2defc0555414a0.png)

**引用：**[https://www.php.net/manual/en/gmagick.setimagetype.php](https://www.php.net/manual/en/gmagick.setimagetype.php)