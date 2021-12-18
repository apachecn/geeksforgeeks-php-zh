# PHP|ImagickDraw setFontStyle()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfontstyle-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfontstyle-function/)

**ImagickDraw：：setFontStyle()**函数是 PHP 中的一个内置函数，用于设置使用文本进行批注时要使用的字体样式。 AnyStyle 枚举充当通配符“无关”选项。

**语法：**

```
*bool* ImagickDraw::setFontStyle( $style )
```

**参数：**此函数接受单个参数*$style*，该参数用于将字体样式的值保存为整数类型。

**样式常量：**

*   发帖主题：Re：Колибри0.7.0
*   Imagick：：style_italic(整数)
*   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
*   Imagick：：Style_Any(整数)

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**ImagickDraw：：setFontStyle()函数**：

**程序 1：**

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font Size
$draw->setFontSize(40);

// Set the Font Style
$draw->setFontStyle(\Imagick::STYLE_OBLIQUE);

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(30);

// Set the text to be added
$draw->annotation(30, 250, "Oblique Style");

// Create new Imagick object     
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(350, 300, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![setFontStyle](img/3b2eabe7a4ab548b715f12ad85a2a358.png)

**程序 2：**

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('black');

// Set the font size
$draw->setFontSize(30);

// Set Font Style
$draw->setFontStyle(\Imagick::STYLE_ITALIC);

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('blue');

// Set the font size
$draw->setFontSize(25);

// Set the text to be added
$draw->annotation(30, 250, "Italic Style");

// Create new Imagick object     
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(350, 300, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![setFontStyle](img/2559125a26630a29a4dca6a670f42898.png)

**引用：**[http://php.net/manual/en/imagickdraw.setfontstyle.php](http://php.net/manual/en/imagickdraw.setfontstyle.php)