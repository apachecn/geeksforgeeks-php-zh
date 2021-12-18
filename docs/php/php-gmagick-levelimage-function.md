# PHP|Gmagick level image()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-levelimage-function/](https://www.geeksforgeeks.org/php-gmagick-levelimage-function/)

**Gmagick：：level image()函数**是 PHP 中的一个内置函数，用于通过将落在指定白点和黑点之间的颜色缩放到全部可用量子范围来调整图像的级别。

**语法：**

```php
*mixed* Gmagick::levelimage( *float* $blackPoint, *float* $gamma,
        *float* $whitePoint, *int* $channel = Gmagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$Blackpoint：**它指定图像黑点。
*   **$Gamma：**它指定图像 Gamma。
*   **$WhitePoint：**它指定图像白点。
*   **$channel(可选)：**它指定对通道模式有效的任何通道常量。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：LevImage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(调整图像级别)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Level the image
$gmagick->levelimage(300000, 8, 10);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/f25017135411b3b8910f7702becf8ad0.png)

**程序 2(标高图形)：**

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
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Level the image
$gmagick->levelimage(0, 34, 30);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/bb45d6cc1056b1147354d5daea4713a5.png)

**引用：**[https://www.php.net/manual/en/gmagick.levelimage.php](https://www.php.net/manual/en/gmagick.levelimage.php)