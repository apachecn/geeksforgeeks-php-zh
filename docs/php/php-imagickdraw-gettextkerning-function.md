# PHP|ImagickDraw getTextKerning()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-gettextkerning-function/](https://www.geeksforgeeks.org/php-imagickdraw-gettextkerning-function/)

**ImagickDraw：：getTextKerning()函数**是 PHP 中的一个内置函数，用于获取图像中使用的文本字距调整，即字母之间的间距。

**语法：**

```
*float* ImagickDraw::getTextKerning( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文本紧排的浮点值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getTextKerning()函数**：

**程序 1：**

```
<?php
// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the text kerning
$textKerning = $draw->getTextKerning();
echo $textKerning;
?>
```

发帖主题：Re：Колибри0.7.0

```
0 // which is the default text kerning.
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the text Kerning
$draw->setTextKerning(5);

// Get the text Kerning
$textKerning = $draw->getTextKerning();
echo $textKerning;
?>
```

发帖主题：Re：Колибри0.7.0

```
5
```

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#eba09b');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotation(50, 100, 
              'The text kerning here is default.');

// Set the text kerning
$draw->setTextKerning(10);

// Annotate a text
$draw->annotation(50, 200, 'The text kerning here is ' 
                      . $draw->getTextKerning() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/aa2f50a49fe26035aaf1476e802ac398.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.gettextkerning.php](https://www.php.net/manual/en/imagickdraw.gettextkerning.php)