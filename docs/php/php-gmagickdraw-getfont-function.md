# PHP|GmagickDraw getfont()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getfont-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getfont-function/)

**GmagickDraw：：getfont()函数**是 PHP 中的一个内置函数，用于获取指定使用文本批注时使用的字体的字符串。

**语法：**

```
*string* GmagickDraw::getfont( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含字体的字符串值。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：getfont()函数**：

**程序 1：**

```
<?php 

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Get the font 
$font = $draw->getfont(); 
echo $font; 
?>
```

发帖主题：Re：Колибри0.7.0

```
Empty string which is the default font.
```

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('yellow');

// Set the font size
$draw->setFontSize(20);

// Set the font to a ttf file which should be
// placed in same folder where the program is.
$draw->setFont('Pacifico.ttf');

// Annotate a text
$draw->annotate(50, 120, 'The Font here is '
    . $draw->getfont() . '.');

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/dfbac03dcfcd961265140161b1378751.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.getfont.php](https://www.php.net/manual/en/gmagickdraw.getfont.php)