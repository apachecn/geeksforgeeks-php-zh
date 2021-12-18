# PHP|Gmagick getimagecolors()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagecolors-function/](https://www.geeksforgeeks.org/php-gmagick-getimagecolors-function/)

**gmagick：：getimagecolors()函数**是 PHP 中的一个内置函数，用于获取图像中唯一颜色的数量。

**语法：**

```
*int* Gmagick::getimagecolors( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回整数值。

**异常：**此函数在出错时引发 GmagickException。

**使用 Image：**捕获下面的画布区域
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)
给定的程序演示了 PHP 中的**Gmagick：：getimagecolors()函数**：

**程序 1：**用于多色图像。

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the border color
$color = $gmagick->getimagecolors();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.0

```
2955
```

**程序 2：**用于单色图像。

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('singlecolor.png');

// Get the border color
$color = $gmagick->getimagecolors();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.0

```
1
```

**程序 3：**用于绘图

```
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

// Get the image colors
$colors = $gmagick->getimagecolors();
echo $colors;
?>
```

发帖主题：Re：Колибри0.7.0

```
238
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagecolors.php](https://www.php.net/manual/en/gmagick.getimagecolors.php)