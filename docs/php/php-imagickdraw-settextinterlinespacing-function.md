# PHP|ImagickDraw setTextInterlineSpacing()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-settextinterlinespacing-function/](https://www.geeksforgeeks.org/php-imagickdraw-settextinterlinespacing-function/)

**ImagickDraw：：setTextInterlineSpacing()函数**是 PHP 中的内置函数，用于设置文本行间间距。

**语法：**

```php
*bool* ImagickDraw::setTextInterlineSpacing( *float* $spacing )
```

**参数：**此函数接受单个参数**$spaceing**，该参数保存文本行间间距。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：setTextInterlineSpacing()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the text interline spacing
$draw->setTextInterLineSpacing(15);

// Get the text interline spacing
$textInterlineSpacing = $draw->getTextInterLineSpacing();
echo $textInterlineSpacing;
?>
```

发帖主题：Re：Колибри0.7.0

```php
15
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(40);

// Set the text interline spacing
$draw->setTextInterLineSpacing(40);

// Annotate a text
$draw->annotation(350, 70, "Geeks \nfor\nGeeks");

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/112e678c58cbecd3138a5e47fb80ab4e.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.settextinterlinespacing.php](https://www.php.net/manual/en/imagickdraw.settextinterlinespacing.php)