# PHP|ImagickDraw getFontFamily()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfontfamily-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfontfamily-function/)

**ImagickDraw：：getFontFamily()函数**是 PHP 中的一个内置函数，用于在注释文本时获取要使用的字体系列。 它告诉您要使用的文本的具体大小和样式，并且有许多字体系列可供选择，如 Times、avantgarde、NewCenturySchlbk、Palatino 等。

**语法：**

```
*string* ImagickDraw::getFontFamily( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含字体系列名称的字符串值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getFontFamily()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font
$draw->setFontFamily("Palatino");

// Get the font
$font = $draw->getFontFamily();
echo $font;
?>
```

发帖主题：Re：Колибри0.7.0

```
Palatino
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'grey');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(50);

// Annotate a text
$draw->annotation(50, 100, 
          'The Font Family here is default.');

// Set the font family
$draw->setFontFamily("sans-sarif");

// Set the font size
$draw->setFontSize(50);

// Annotate a text
$draw->annotation(50, 200, 
                  'The Font Family here is ' 
                  . $draw->getFontFamily() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/eaa7a58fbee409ee6dc41837add60c6d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getfontfamily.php](https://www.php.net/manual/en/imagickdraw.getfontfamily.php)