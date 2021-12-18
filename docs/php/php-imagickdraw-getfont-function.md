# PHP|ImagickDraw getFont()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfont-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfont-function/)

**ImagickDraw：：getFont()函数**是 PHP 中的一个内置函数，用于获取指定使用文本进行批注时使用的字体的字符串。

**语法：**

```
*string* ImagickDraw::getFont( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含字体名称的字符串值。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickDraw：：getFont()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the font
$font = $draw->getFont();
echo $font;
?>
```

发帖主题：Re：Колибри0.7.0

```
Empty string which is the default font.
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font to a font file name which
// should be present in the same folder
$draw->setFont('roboto.ttf');

// Get the font
$font = $draw->getFont();
echo $font;
?>
```

发帖主题：Re：Колибри0.7.0

```
/home/user/php/roboto.ttf
```

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'yellow');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(30);

// Annotate a text
$draw->annotation(50, 100, 'The Font here is default.');

// Set the font to a ttf file which should be
// placed in same folder where the program is.
$draw->setFont('Pacifico.ttf');

// Annotate a text
$draw->annotation(50, 200, 'The Font here is '
          . $draw->getFont() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/c01da5002e50c5aae91e6fc4e7171f81.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getfont.php](https://www.php.net/manual/en/imagickdraw.getfont.php)