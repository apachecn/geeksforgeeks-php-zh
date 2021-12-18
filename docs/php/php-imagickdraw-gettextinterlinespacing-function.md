# PHP|ImagickDraw getTextInterlineSpacing()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-gettextinterlinespacing-function/](https://www.geeksforgeeks.org/php-imagickdraw-gettextinterlinespacing-function/)

**ImagickDraw：：getTextInterlineSpacing()函数**是 PHP 中的一个内置函数，用于获取文本行间间距。 数字越大，空间就越大。 默认间距为 0。

**语法：**

```php
*float* ImagickDraw::getTextInterlineSpacing( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文本行间间距的浮点值。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickDraw：：getTextInterlineSpacing()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the text interline spacing
$textInterlineSpacing = $draw->getTextInterLineSpacing();
echo $textInterlineSpacing;
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

// Set the text interline spacing
$draw->setTextInterLineSpacing(50);

// Get the text interline spacing
$textInterlineSpacing = $draw->getTextInterLineSpacing();
echo $textInterlineSpacing;
?>
```

发帖主题：Re：Колибри0.7.0

```php
50
```

**程序 3：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'brown');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('white');

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotation(50, 100, "The text interterline \nspacing here is "
            . $draw->getTextInterLineSpacing());

// Set the text interline spacing
$draw->setTextInterLineSpacing(30);

// Annotate a text
$draw->annotation(300, 100, "The text interterline \nspacing here is "
            . $draw->getTextInterLineSpacing());

// Set the text interline spacing
$draw->setTextInterLineSpacing(50);

// Annotate a text
$draw->annotation(550, 100, "The text interterline \nspacing here is "
            . $draw->getTextInterLineSpacing());

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/9da9aa86f9792ba5527c8d4cfe80a886.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.gettextinterlinespacing.php](https://www.php.net/manual/en/imagickdraw.gettextinterlinespacing.php)