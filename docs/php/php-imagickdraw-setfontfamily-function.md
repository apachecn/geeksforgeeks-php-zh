# PHP|ImagickDraw setFontFamily()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfontfamily-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfontfamily-function/)

**ImagickDraw：：setFontFamily()**函数是 PHP 中的一个内置函数，用于设置使用文本进行批注时要使用的字体系列。

**语法：**

```
*bool* ImagickDraw::setFontFamily( $font_family )
```

**参数：**此函数接受单个参数*$font_family*，该参数用于将字体系列的值保存为字符串。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**ImagickDraw：：setFontFamily()函数**：

**程序 1：**

## PHP

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font size
$draw->setFontSize(40);

// Set the Font Family
$draw->setFontFamily('Ubuntu-Mono');

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(30);

// Set the Font Family
$draw->setFontFamily('Open-Sans-Light-Italic');

// Set the text to be added
$draw->annotation(30, 250, "Ubuntu-Mono");

// Create new imagick object   
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(350, 300, 'white');

// Set the image formats
$imagick->setImageFormat("png");

// Draw the image
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![setFontFamily](img/5e8c255c1df155d110015a963d900734.png)

**程序 2：**

## PHP

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// set the image filled color
$draw->setFillColor('Green');

// Set the font size
$draw->setFontSize(30);

// Set the Font Style
$draw->setFontFamily('Ani');

// Set the text to be added
$draw->annotation(30, 40, "GeeksForGeeks");

// Create new imagick object   
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(250, 70, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![setFontFamily](img/8f1da15a495177591e06a422e485ca4c.png)

**引用：**[http://php.net/manual/en/imagickdraw.setfontfamily.php](http://php.net/manual/en/imagickdraw.setfontfamily.php)