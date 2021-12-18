# PHP|ImagickDraw setFontWeight()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfontweight-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfontweight-function/)

**ImagickDraw：：setFontWeight()**函数是 PHP 中的内置函数，用于设置字体粗细。

**语法：**

```php
*bool* ImagickDraw::setFontWeight( $font_weight )
```

**参数：**此函数接受单个参数*$font_weight*，该参数用于将字体粗细的值保存为整数类型。

**返回值：**成功时此函数返回 True。

下面的程序说明了 PHP 中的**ImagickDraw：：setFontWeight()函数**：

**程序 1：**

```php
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('red');

// Set the Font Weight
$draw->setFontWeight(200);

// Set the font size
$draw->setFontSize(40);

// Set the font family
$draw->setFontFamily('Ubuntu-Mono');

// Set the text to be added
$draw->annotation(30, 170, "GeeksForGeeks");

// Set the image filled color
$draw->setFillColor('green');

// Set the Font Stretch
$draw->setFontStretch(3);

// Set the font size
$draw->setFontSize(30);

// Set the font family
$draw->setFontFamily('Open-Sans-Light-Italic');

// Set the text to be added
$draw->annotation(30, 250, "Font-Weight : 200");

// Create new imagick object    
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
![setFontWeight](img/45b9954d95845d42c2686134210f5ce5.png)

**程序 2：**

```php
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color
$draw->setFillColor('Green');

// Set the font size
$draw->setFontSize(30);

// Set the Font Weight
$draw->setFontWeight(400);

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

**输出：**
![setFontWeight](img/9c23154fd4bfe6740da2a13f574fc601.png)

**引用：**[http://php.net/manual/en/imagickdraw.setfontweight.php](http://php.net/manual/en/imagickdraw.setfontweight.php)