# PHP|ImagickDraw getFontStyle()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfontstyle-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfontstyle-function/)

**ImagickDraw：：getFontStyle()函数**是 PHP 中的一个内置函数，用于获取使用文本进行批注时使用的字体样式。

**语法：**

```
*int* ImagickDraw::getFontStyle( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，该值对应于[样式常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.style-normal)之一，或者在未设置样式时返回 0。
样式常量列表如下：

*   Imagick：：Style_Normal(1)
*   Imagick：：style_italic(2)
*   Imagick：：Style_Interique(3)
*   Imagick：：Style_Any(4)

下面的程序演示了 PHP 中的**ImagickDraw：：getFontStyle()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the font Style
$fontStyle = $draw->getFontStyle();
echo $fontStyle;
?>
```

发帖主题：Re：Колибри0.7.0

```
0 // Which is default value.
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font Style
$draw->setFontStyle(imagick::STYLE_OBLIQUE);

// Get the font Style
$fontStyle = $draw->getFontStyle();
echo $fontStyle;
?>
```

发帖主题：Re：Колибри0.7.0

```
3
```

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#bfc7d6');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(30);

// Annotate a text
$draw->annotation(50, 100, 
     'The Font style here is default.');

// Set the font style
$draw->setFontStyle(imagick::STYLE_ITALIC);

// Annotate a text
$draw->annotation(50, 200, 'The Font style here is '
        . $draw->getFontStyle() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/2b12244c8d419caf329b29a3d7320904.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getfontstyle.php](https://www.php.net/manual/en/imagickdraw.getfontstyle.php)