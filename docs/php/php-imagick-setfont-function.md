# PHP|Imagick setFont()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setfont-function/](https://www.geeksforgeeks.org/php-imagick-setfont-function/)

**Imagick：：setFont()函数**是 PHP 中用于设置字体的内置函数。

**语法：**

```php
*bool* Imagick::setFont( *string* $font )
```

**参数：**此函数接受保存字体文件名称的单个参数**$font**。

**返回值：**如果成功，此函数返回 TRUE。

**扩展：此功能需要安装**GD 扩展。

下面的程序演示了 PHP 中的**Imagick：：getFont()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Use setFont() function to set the
// font using .ttf font file. The .ttf
// file is placed in same folder
$imagick->setFont('Windsong.ttf'); 

// Write a caption in image format
$imagick->newPseudoImage(800, 350, "caption:GeekforGeeks");

// Show the output
$imagick->setformat('png');

header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/91b143d711442fdf1d0d85a437311738.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the font - make sure .ttf font file 
// is placed in same folder
$imagick->setFont('FFF_Tusj.ttf'); 

// Write the caption in a image
$imagick->newPseudoImage(800, 350, "caption:GeekforGeeks");

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/eb21e277dd14559ecbc48864460e33a2.png)

**引用：**[https://www.php.net/manual/en/imagick.setfont.php](https://www.php.net/manual/en/imagick.setfont.php)