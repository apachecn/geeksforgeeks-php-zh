# PHP|GmagickDraw 注解()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-annotate-function/](https://www.geeksforgeeks.org/php-gmagickdraw-annotate-function/)

**GmagickDraw：：Annotate()函数**是 PHP 中的一个内置函数，用于在图像上绘制文本。

**语法：**

```php
*GmagickDraw* GmagickDraw::annotate( *float* $x, *float* $y, *string* $text )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$x：**它指定文本的 x 坐标。
*   **$y：**它指定文本的 y 坐标。
*   **$text：**它指定文本内容。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**GmagickDraw：：Annotate()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(向图形添加文本)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('red');

// Set the font size
$draw->setfontsize(80);

// Annotate a text
$draw->annotate(30, 120, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/bf157c739199b3a055c3bc1704a52ba9.png)

**程序 2(向图像添加文本)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the fill color
$draw->setFillColor('green');

// Set the font size
$draw->setfontsize(30);

// Annotate a text
$draw->annotate(100, 120, 
    'This line is drawn with annotate');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/7ee349420a6e8a05feedcb79291b69a9.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.annotate.php](https://www.php.net/manual/en/gmagickdraw.annotate.php)