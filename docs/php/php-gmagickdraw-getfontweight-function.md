# PHP|GmagickDraw getfontweight()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getfontweight-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getfontweight-function/)

**GmagickDraw：：getfontweight()函数**是 PHP 中的一个内置函数，用于获取在注释文本时使用的字体粗细。 字体粗细实际上表示字体的粗体，字体粗细越大，文本越粗体。 它可以是从 100 到 900 的任何值。

**语法：**

```
*int* GmagickDraw::getfontweight( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含字体粗细的整数值。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：getfontweight()函数**：

**程序 1：**

```
<?php

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Get the font Weight 
$fontWeight = $draw->getfontweight(); 
echo $fontWeight; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
0 // Which is the default value
```

**程序 2：**

```
<?php 

// Create a new GmagickDraw object 
$draw = new GmagickDraw(); 

// Set the font weight
$draw->setfontweight(200);

// Get the font Weight 
$fontWeight = $draw->getfontweight(); 
echo $fontWeight; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
200
```

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 3：**

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

// Set the font weight
$draw->setFontWeight(900);

// Annotate a text
$draw->annotate(50, 100,
    'The Font weight here is '
    . $draw->getFontWeight() . '.');

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/4a0a2327fe1425d2ac09b1f9fb62fbaa.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.getfontweight.php](https://www.php.net/manual/en/gmagickdraw.getfontweight.php)