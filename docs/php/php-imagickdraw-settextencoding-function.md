# PHP|ImagickDraw setTextEncoding()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-settextencoding-function/](https://www.geeksforgeeks.org/php-imagickdraw-settextencoding-function/)

**ImagickDraw：：setTextEncoding()函数**是 PHP 中的一个内置函数，用于设置用于文本注释的代码集。 这些代码集告诉计算机如何将原始的 0 和 1 解释为真正的字符。 通常，它们生成相同的文本，但使用不同的代码集。

**语法：**

```php
*bool* ImagickDraw::setTextEncoding( *string* $encoding_name )
```

**参数：**此函数接受单个参数**$ENCODING_NAME**，该参数保存代码集的名称。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：setTextEncoding()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the text encoding
$draw->setTextEncoding('UTF-16');

// Get the text encoding
$textEncoding = $draw->getTextEncoding();
echo $textEncoding;
?>
```

发帖主题：Re：Колибри0.7.0

```php
UTF-16
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('skyblue');

// Set the font size
$draw->setFontSize(40);

// Set the text encoding
$draw->setTextEncoding('UTF-8');

// Annotate a text
$draw->annotation(50, 150, 'This text is encoded in UTF-8.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/2e7e097a0c26f4e4397f5a86d7cad499.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.settextencoding.php](https://www.php.net/manual/en/imagickdraw.settextencoding.php)