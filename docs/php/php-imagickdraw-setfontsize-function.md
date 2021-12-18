# PHP|ImagickDraw setFontSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfontsize-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfontsize-function/)

**ImagickDraw：：setFontSize()**函数是 PHP 中的内置函数，用于设置字体磅值。 它在使用文本进行批注时使用。

**语法：**

```php
*bool* ImagickDraw::setFontSize( $pointsize )
```

**参数：**此函数接受单个参数*$pointsize*，该参数用于保存点大小的值。
**返回值：**此函数不返回任何值。
下面的程序说明 PHP：
**程序 1：**中的**ImagickDraw：：setFontSize()函数**

## PHP

```php
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('Green');

// Set the Font Size
$draw->setFontSize(30);

// Set the font family
$draw->setFontFamily('Ani');

// Set the text to be added
$draw->annotation(30, 40, "GeeksForGeeks");

// Create new Imagick object
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

发帖主题：Re：Колибри0.7.0

![setFontSize](img/8f1da15a495177591e06a422e485ca4c.png)

**程序 2：**

## PHP

```php
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font Size
$draw->setFontSize(40);

// Set the Font family
$draw->setFontFamily('Ubuntu-Mono');

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(30);

// Set the font family
$draw->setFontFamily('Open-Sans-Light-Italic');

// Set the text to be added
$draw->annotation(30, 250, "Ubuntu-Mono");

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

发帖主题：Re：Колибри0.7.0

![setFontSize](img/5e8c255c1df155d110015a963d900734.png)

**引用：**[http://php.net/manual/en/imagickdraw.setfontsize.php](http://php.net/manual/en/imagickdraw.setfontsize.php)