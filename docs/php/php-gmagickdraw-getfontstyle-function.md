# PHP|GmagickDraw getfontstyle()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getfontstyle-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getfontstyle-function/)

**GmagickDraw：：getfontstyle()函数**是 PHP 中的一个内置函数，用于获取在注释文本时使用的字体样式。

**语法：**

```
*int* GmagickDraw::getfontstyle( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与[样式常量](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.style-normal)之一相对应的整数值。
样式常量列表如下：

*   Gmagick：：STYLE_NORMAL(整数)
*   Gmagick：：style_italic(整数)
*   Gmagick：：style_oblique(整数)
*   Gmagick：：Style_Any(整数)

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：getfontstyle()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Get the font Style 
$fontStyle = $draw->getfontstyle(); 
echo $fontStyle; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
0 // Which is the default value.
```

**程序 3：**

```
<?php

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Set the font style
$draw->setfontstyle(2);

// Get the font Style 
$fontStyle = $draw->getfontstyle(); 
echo $fontStyle; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
2
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('#0E0E0E');

// Set the font size
$draw->setfontsize(40);

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the font style to Italic
$draw->setFontStyle(Gmagick::STYLE_ITALIC);

// Annotate a text
$draw->annotate(50, 100, 'The Font style here is '
    . $draw->getFontStyle() . '.');

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/04a5cb196211958832711a145fd80697.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.getfontstyle.php](https://www.php.net/manual/en/gmagickdraw.getfontstyle.php)