# PHP|Imagick SegmentImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-segmentimage-function/](https://www.geeksforgeeks.org/php-imagick-segmentimage-function/)

**Imagick：：SegmentImage()函数**是 PHP 中的一个内置函数，用于分割图像。

**语法：**

```php
*bool* Imagick::segmentImage(*int* $COLORSPACE, 
*float* $cluster_threshold, *float* $smooth_threshold, 
*bool* $verbose = FALSE )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$Colorspace：**它指定与**Colorspace**常量之一对应的整数值。 还可以传递直接常量，如*Imagick：：Colorspace_RGB*。
*   **$CLUSTER_THRESHOLD：**它指定一个百分比，用于描述十六进制中包含的最小像素数，然后将其视为有效。
*   **$Smooth_Threshold：**它指定是否从直方图中消除噪声。
*   **$Verbose(可选)：**它指定是否输出有关已识别类的详细信息。 默认值为 False

下面给出了所有颜色空间常量的列表：

*   Imagick：：Colorspace_ 未定义(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Colorspace_Gray(2)
*   Imagick：：Colorspace_Transparent(3)
*   Imagick：：Colorspace_Ohta(4)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Colorspace_YCBCR(7)
*   Imagick：：Colorspace_YCC(8)
*   Imagick：：Colorspace_YIQ(9)
*   Imagick：：Colorspace_YPBPR(10)
*   Imagick：：Colorspace_YUV(11)
*   发帖主题：Re：Колибри0.7.0
*   Imagick：：Colorspace_SRGB(13)
*   Imagick：：Colorspace_HSB(14)
*   Imagick：：Colorspace_HSL(15)
*   Imagick：：Colorspace_hwb(16)
*   Imagick：：Colorspace_REC601LUMA(17)
*   Imagick：：Colorspace_REC709LUMA(19)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   发帖主题：Re：Колибри0.7.0

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：SegmentImage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Segment the image with colorspace as imagick::COLORSPACE_RGB
$imagick->segmentImage(1, 0, 12);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/605bd456a827818e8c0ccde51ae405ca.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Segment the image with colorspace as imagick::COLORSPACE_GRAY
$imagick->segmentImage(2, 5, 30);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/88f3155474318c88508f36b4e0126d7e.png)

**引用：**[https://www.php.net/manual/en/imagick.segmentimage.php](https://www.php.net/manual/en/imagick.segmentimage.php)