# PHP|GmagickDraw getttencoding()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-gettextencoding-function/](https://www.geeksforgeeks.org/php-gmagickdraw-gettextencoding-function/)

**GmagickDraw：：getttencoding()函数**是 PHP 中的一个内置函数，用于获取用于文本注释的代码集。 这些代码集告诉计算机如何将原始的 0 和 1 解释为真正的字符。 通常，它们生成相同的文本，但使用不同的代码集。

**语法：**

```
*string* GmagickDraw::gettextencoding( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含所用文本编码的字符串值。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：gettextcoding()函数**：

**程序 1：**

```
<?php

// Create a new GmagickDraw object
$draw = new GmagickDraw();

// Get the text encoding
$textEncoding = $draw->gettextencoding();
echo $textEncoding;
?>
```

发帖主题：Re：Колибри0.7.0

```
// Empty string which is the default value
```

**程序 2：**

```
<?php

// Create a new GmagickDraw object
$draw = new GmagickDraw();

// Set the text encoding
$draw->settextencoding('utf-8');

// Get the text encoding
$textEncoding = $draw->gettextencoding();
echo $textEncoding;
?>
```

发帖主题：Re：Колибри0.7.0

```
utf-8
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

// Draw rectangle for background
$draw->rectangle(-10, -10, 800, 400);

// Set the font size
$draw->setFontSize(40);

// Set the fill color
$draw->setfillcolor('white');

// Set the text encoding
$draw->settextencoding('UTF-8');

// Annotate a text
$draw->annotate(50, 50,
    'This line is encoded with '
    . $draw->getTextEncoding());

// Set the text encoding
$draw->settextencoding('UTF-32');

// Annotate a text
$draw->annotate(50, 100,
    'This line is encoded with '
    . $draw->getTextEncoding());

// Use of drawimage functeannotate
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/ead9ac9be84f36f5e1d5a28f7c7ef57c.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.gettextencoding.php](https://www.php.net/manual/en/gmagickdraw.gettextencoding.php)