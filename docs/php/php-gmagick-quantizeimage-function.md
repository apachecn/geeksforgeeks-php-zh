# PHP|Gmagick 量化图像()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-quantizeimage-function/](https://www.geeksforgeeks.org/php-gmagick-quantizeimage-function/)

**Gmagick：：QuantizeImage()函数**是 PHP 中的一个内置函数，用于分析参考图像中的颜色，并选择固定数量的颜色来表示图像。 此功能的主要原因是在最小化处理时间的同时最小化输入和输出图像之间的色差。

**语法：**

```
*Gmagick* Gmagick::quantizeimage( *int* $numColors, *int* $colorspace,
          *int* $treeDepth, *bool* $dither, *bool* $measureError )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$numColors：**它指定颜色的数量。
*   **$Colorspace：**它指定颜色空间。
*   **$treeDepth：**它指定树的深度。
*   **$dither：**它指定是否允许抖动。
*   **$measure Error：**它指定是否测量图像差异误差。

**返回值：**此函数在成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：QuantizeImage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

[]T0−程序 1(量化图像)：ΔT1*

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Quantize the image
$gmagick->quantizeimage(100, 8, 256, true, false);

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/438824d9f5ff66b7d850eeffc61b8ed3.png)

**程序 2(量化图形)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('red');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('white');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Quantize the image
$gmagick->quantizeimage(10, 8, 996, true, false);

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/e61d65fde683086926bcae25a83e7eaa.png)

**引用：**[https://www.php.net/manual/en/gmagick.quantizeimage.php](https://www.php.net/manual/en/gmagick.quantizeimage.php)