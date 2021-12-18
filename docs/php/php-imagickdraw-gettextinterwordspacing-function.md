# PHP|ImagickDraw getTextInterwordSpacing()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-gettextinterwordspacing-function/](https://www.geeksforgeeks.org/php-imagickdraw-gettextinterwordspacing-function/)

**ImagickDraw：：getTextInterwordSpacing()函数**是 PHP 中的一个内置函数，用于获取文本的单词间间距，即每个单词之间的间距。 数字越大，包含的空间就越大。 默认间距为 0。

**语法：**

```php
*float* ImagickDraw::getTextInterwordSpacing( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文本字间间距的浮点值。

下面的程序演示了 PHP 中的**ImagickDraw：：getTextInterwordSpacing()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the text interword spacing
$textInterwordSpacing = $draw->getTextInterwordSpacing();
echo $textInterwordSpacing;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0 // Which is the default value
```

**程序 2：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the text interword spacing
$draw->setTextInterWordSpacing(30);

// Get the text interword spacing
$textInterwordSpacing = $draw->getTextInterwordSpacing();
echo $textInterwordSpacing;
?>
```

发帖主题：Re：Колибри0.7.0

```php
30
```

**程序 3：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, '#c0eb34');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotation(50, 80, "The text interterword spacing here is "
           . $draw->getTextInterwordSpacing());

// Set the text interword spacing
$draw->setTextInterwordSpacing(20);

// Annotate a text
$draw->annotation(50, 120, "The text interterword spacing here is "
            . $draw->getTextInterwordSpacing());

// Set the text interword spacing
$draw->setTextInterwordSpacing(35);

// Annotate a text
$draw->annotation(50, 160, "The text interterword spacing here is "
           . $draw->getTextInterwordSpacing());

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/0d89d272d2356ee3f31227bfa00cc54d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.gettextinterwordspacing.php](https://www.php.net/manual/en/imagickdraw.gettextinterwordspacing.php)