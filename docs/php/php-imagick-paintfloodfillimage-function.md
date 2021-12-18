# PHP|Imagick pairtFlodFillImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-paintfloodfillimage-function/](https://www.geeksforgeeks.org/php-imagick-paintfloodfillimage-function/)

函数**的函数**是 PHP 中的一个内置函数，用于更改与目标匹配且是其直接邻居的任何像素的颜色值。

**语法：**

```
*bool* Imagick::paintFloodFillImage( $fill, $fuzz, $bordercolor, 
                                   $x, $y, $channel = Imagick::CHANNEL_DEFAULT )

```

**注意：**此函数将替换为**[Imagick：：fuldFillPaintImage()函数](https://www.geeksforgeeks.org/php-imagick-floodfillpaintimage-function/)**。

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$Fill：**它保存 ImagickPixel 对象或字符串值来填充颜色。
*   **$fuzz：**它定义了模糊量。
*   **$borderColor：**它保存 ImagickPixel 对象或边框像素颜色的字符串值。
*   **$x：**它包含填方体 x 轴的起始位置。
*   **$y：**它包含填方体 y 轴的起始位置。
*   **$INVERT：**它包含布尔值**TRUE**或**FALSE**。 **true**绘制与目标颜色不匹配的任何像素。
*   **$channel：**它包含通道常量。 可以使用按位运算符组合多个通道常量。

**返回值：**此函数成功时返回**true**。

下面的程序演示了 PHP 中的 Imagick：：FilldFillPaintImage()函数：

**程序：**

```
<?php 

// Creating an imagick object
$img = new Imagick(
'https://cdncontribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png'); 

// Use Imagick::paintFloodFillImage() function to change the 
// color value of the target color
$img->floodFillPaintImage('cyan', 1, 'white', 1, 1, false); 

header("Content-Type: image/png"); 

// Display the output image 
echo $img->getImageBlob(); 
?>
```

**输出：**
![paintFloodFillImage()](img/0dc169c14c14740c079c2550f1e0b01b.png)

**引用：**[https://www.php.net/manual/en/imagick.paintfloodfillimage.php](https://www.php.net/manual/en/imagick.paintfloodfillimage.php)