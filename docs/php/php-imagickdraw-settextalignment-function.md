# PHP|ImagickDraw setTextAlign()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-settextalignment-function/](https://www.geeksforgeeks.org/php-imagickdraw-settextalignment-function/)

**ImagickDraw：：setTextAlign()**函数是 PHP 中的一个内置函数，用于指定文本左对齐、居中对齐或右对齐。

**语法：**

```
*bool* ImagickDraw::setTextAlignment( $alignment )
```

**参数：**此函数接受单个参数*$alignment*，该参数用于保存 ALIGN_CONSTANNTS 的值。

ALIGN_CONTAINT 列表如下所示：

*   Imagick：：ALIGN_UNDEFINED(整数)
*   Imagick：：Align_Left(整数)
*   Imagick：：ALIGN_CENTER(整数)
*   Imagick：：Align_Right(整数)

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**ImagickDraw：：setTextAlign()函数**：

**程序：**

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color 
$draw->setFillColor('white');

// Set the Font size
$draw->setFontSize(40);

// Set the text Alignment
$draw->setTextAlignment(0);

// Set the text to be added
$draw->annotation(110, 75, "GeeksforGeeks!");

// Set the text alignment 
$draw->setTextAlignment(1);

// Set the Font size
$draw->setFontSize(20);

// Set the text to be added
$draw->annotation(100, 110, "A computer science portal for geeks");

// Create new imagick object
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(500, 300, 'green');

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
![setTextAlignment](img/8acb4765e4efb89d7e2bbd86e2ccd505.png)

**引用：**[http://php.net/manual/en/imagickdraw.settextalignment.php](http://php.net/manual/en/imagickdraw.settextalignment.php)