# PHP|GmagickDraw setttencoding()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-settextencoding-function/](https://www.geeksforgeeks.org/php-gmagickdraw-settextencoding-function/)

**GmagickDraw：：setttencoding()函数**是 PHP 中的一个内置函数，用于设置用于文本注释的代码集。 这些代码集告诉计算机如何将原始的 0 和 1 解释为真正的字符。 通常，它们生成相同的文本，但使用不同的代码集。

**语法：**

```php
*GmagickDraw* GmagickDraw::settextencoding( *string* $encoding )
```

**参数：**此函数接受保存编码的单个参数**$coding**。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序说明了 PHP：
**程序 1：**中的**GmagickDraw：：setttencoding()函数**

```php
<?php
// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the encoding
$draw->settextencoding('utf-32');

// Get the encoding
$encoding = $draw->gettextencoding();
echo $encoding;
?>
```

发帖主题：Re：Колибри0.7.0

```php
utf-32
```

**程序 2：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-100, -1000, 800, 400);

// Set the fill color
$draw->setfillcolor('white');

// Set the font size
$draw->setfontsize(30);

// Set the stroke color
$draw->setstrokecolor('green');

// Set the encoding
$draw->settextencoding('utf-8');

// Create a rectangle
$draw->annotate(20, 110, 'This text is encoded using ' . $draw->gettextencoding());

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/63150c9681ed39381e1ee5617443788d.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.settextencoding.php](https://www.php.net/manual/en/gmagickdraw.settextencoding.php)