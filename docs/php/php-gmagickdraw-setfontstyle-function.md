# PHP|GmagickDraw setfontstyle()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfontstyle-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfontstyle-function/)

GmagickDraw：：setfontstyle()函数是 PHP 中的一个内置函数，用于设置使用文本进行批注时要使用的字体样式。 样式枚举充当通配符无关选项。

**语法：**

```php
 *public* GmagickDraw::setfontstyle( $style ) : GmagickDraw
```

**参数：**此函数接受单个参数*$style*，该参数用于将字体样式的值保存为整数类型。

**样式常量：**样式常量列表如下：

*   Gmagick：：STYLE_NORMAL(整数)
*   Gmagick：：style_italic(整数)
*   Gmagick：：style_oblique(整数)
*   Gmagick：：Style_Any(整数)

**返回值：**此函数成功时返回 GmagickDraw 对象。

下面的程序演示了 PHP 中的 GmagickDraw：：setfontstyle()函数：

**程序 1：**

```php
<?php

// Create an GmagickDraw object
$draw = new GmagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font Size
$draw->setFontSize(40);

// Set the Font Style
$draw->setfontstyle(\Gmagick::STYLE_OBLIQUE);

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(30);

// Set the text to be added
$draw->annotation(30, 250, "Oblique Style");

// Create new Gmagick object     
$gmagick= new Gmagick();

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
![setFontStyle](img/3b2eabe7a4ab548b715f12ad85a2a358.png)

**程序 2：**

```php
<?php

// Create an GmagickDraw object
$draw = new GmagickDraw();

// Set the image filled color
$draw->setFillColor('black');

// Set the font size
$draw->setFontSize(30);

// Set Font Style
$draw->setfontstyle(\Gmagick::STYLE_ITALIC);

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('blue');

// Set the font size
$draw->setFontSize(25);

// Set the text to be added
$draw->annotation(30, 250, "Italic Style");

// Create new Gmagick object     
$gmagick= new Gmagick();

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
![setFontStyle](img/2559125a26630a29a4dca6a670f42898.png)

**引用：**[http://php.net/manual/en/gmagickdraw.setfontstyle.php](http://php.net/manual/en/gmagickdraw.setfontstyle.php)