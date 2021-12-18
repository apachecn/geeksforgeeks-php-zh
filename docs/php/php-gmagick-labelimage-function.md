# PHP|Gmagick labelimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-labelimage-function/](https://www.geeksforgeeks.org/php-gmagick-labelimage-function/)

**Gmagick：：labelimage()函数**是 PHP 中的一个内置函数，用于标记图像。 标签只是贴在图像上的字符串，稍后可以从图像中提取回来。 此标签在图像本身上不可见，但您可以使用*Annotate*函数执行此操作。

**语法：**

```
*mixed* Gmagick::labelimage( *string* $label )
```

**参数：**此函数接受保存图像标签的单个参数**$label**。

**返回值：**此函数返回带有标签的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：labelimage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

$label = "Hello World";

// Label the image
$gmagick->labelimage($label);

// Get the label from image
$label = substr($gmagick, -28, strlen($label) + 1);
echo $label;
?>
```

发帖主题：Re：Колибри0.7.0

```
Hello World
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

$label = "This is my label";

// Label the image
$gmagick->labelimage($label);

// Get the label from image
$getlabel = substr($gmagick, -32, strlen($label));

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('orange');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, $getlabel);

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/25771c07181be1bc3f7f6c8031404a92.png)

**引用：**[https://www.php.net/manual/en/gmagick.labelimage.php](https://www.php.net/manual/en/gmagick.labelimage.php)