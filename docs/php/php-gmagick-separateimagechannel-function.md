# PHP|Gmagick 分离图像通道()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-separateimagechannel-function/](https://www.geeksforgeeks.org/php-gmagick-separateimagechannel-function/)

**Gmagick：：Separateimagecnel()函数**是 PHP 中的一个内置函数，用于将通道从图像中分离出来，并返回灰度图像。 通道是图像中每个像素的特定颜色分量。

**语法：**

```
*Gmagick* Gmagick::separateimagechannel( *int* $channel )
```

**参数：**此函数接受单个参数**$channel**，该参数保存与通道常量之一相对应的整数值。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：Separateimagecnel()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(分隔红色通道)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Separate the Gmagick::CHANNEL_RED
$gmagick->separateimagechannel(Gmagick::CHANNEL_RED);

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/2e7b1023fb1265fc3ca35bd376a819b2.png)

**程序 2(分隔绿色通道)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Separate the Gmagick::CHANNEL_GREEN
$gmagick->separateimagechannel(Gmagick::CHANNEL_GREEN);

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/2b56f0b2bf08dd85b193dc56c794d9b7.png)

**程序 3(用于绘图)：**

```
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
$draw->setFillColor('yellow');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Separate the Gmagick::CHANNEL_BLUE
$gmagick->separateimagechannel(Gmagick::CHANNEL_BLUE);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/a80d25d09ab7c8c01b80f9f12c9d2b4a.png)

**引用：**[https://www.php.net/manual/en/gmagick.separateimagechannel.php](https://www.php.net/manual/en/gmagick.separateimagechannel.php)