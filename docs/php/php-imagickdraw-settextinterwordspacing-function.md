# PHP|ImagickDraw setTextInterwordSpacing()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-settextinterwordspacing-function/](https://www.geeksforgeeks.org/php-imagickdraw-settextinterwordspacing-function/)

**ImagickDraw：：setTextInterwordSpacing()函数**是 PHP 中的一个内置函数，用于设置文本的单词间间距，即每个单词之间的间距。 数字越大，空间就越大。 默认间距为 0。

**语法：**

```php
*bool* ImagickDraw::setTextInterwordSpacing( *float* $spacing )
```

**参数：**此函数接受单个参数**$spaceing**，该参数保存文本字间间距。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：setTextInterwordSpacing()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the text interword spacing
$draw->setTextInterWordSpacing(40);

// Get the text interword spacing
$textInterwordSpacing = $draw->getTextInterwordSpacing();
echo $textInterwordSpacing;
?>
```

发帖主题：Re：Колибри0.7.0

```php
40
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#1cced4');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(50);

// Set the text interword spacing
$draw->setTextInterwordSpacing(65);

// Annotate a text
$draw->annotation(150, 140, "Geeks for Geeks");

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/fab7411fc247b6e686b1cc3c73a70a12.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.settextinterwordspacing.php](https://www.php.net/manual/en/imagickdraw.settextinterwordspacing.php)