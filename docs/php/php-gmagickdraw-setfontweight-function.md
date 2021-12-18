# PHP|GmagickDraw setfontweight()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfontweight-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfontweight-function/)

GmagickDraw：：setfontweight()函数是 PHP 中的一个内置函数，用于设置字体粗细。

**语法：**

```
 *public* GmagickDraw::setfontweight( $font_weight ) : GmagickDraw
```

**参数：**此函数接受单个参数*$font_weight*，该参数用于将字体粗细的值保存为整数类型。

**返回值：**此函数在成功时返回 GmagickDraw 对象。

下面的程序演示了 PHP 中的 GmagickDraw：：setfontweight()函数：

**程序 1：**

```
<?php

// Create an GmagickDraw object
$draw = new GmagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font Weight
$draw->setFontWeight(200);

// Set the font size
$draw->setFontSize(40);

// Set the font family
$draw->setFontFamily('Ubuntu-Mono');

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the Font Stretch
$draw->setFontStretch(3);

// Set the font size
$draw->setFontSize(30);

// Set the font family
$draw->setFontFamily('Open-Sans-Light-Italic');

// Set the text to be added
$draw->annotation(30, 250, "Font-Weight : 200");

// Create new gmagick object    
$gmagick = new Gmagick();

// Set the image dimension 
$gmagick->newImage(350, 300, 'white');

// Set the image format
$gmagick->setImageFormat("png");

// Draw the image 
$gmagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $gmagick->getImageBlob();
?>
```

**输出：**
![setFontWeight](img/45b9954d95845d42c2686134210f5ce5.png)

**程序 2：**

```
<?php

// Create an GmagickDraw object
$draw = new GmagickDraw();

// Set the image filled color
$draw->setFillColor('Green');

// Set the font size
$draw->setFontSize(30);

// Set the Font Weight
$draw->setFontWeight(400);

// Set the font family
$draw->setFontFamily('Ani');

// Set the text to be added
$draw->annotation(30, 40, "GeeksForGeeks");

// Create new Gmagick object    
$gmagick= new Gmagick();

// Set the image dimension
$gmagick->newImage(250, 70, 'white');

// Set the image format
$gmagick->setImageFormat("png");

// Draw the image
$gmagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $gmagick->getImageBlob();
?>
```

**输出：**
![setFontWeight](img/9c23154fd4bfe6740da2a13f574fc601.png)

**引用：**[http://php.net/manual/en/gmagickdraw.setfontweight.php](http://php.net/manual/en/gmagickdraw.setfontweight.php)