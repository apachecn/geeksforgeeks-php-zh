# PHP|Imagick setImageColorspace()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagecolorspace-function/](https://www.geeksforgeeks.org/php-imagick-setimagecolorspace-function/)

**Imagick：：setImageColorspace()函数**是 PHP 中的内置函数，用于设置图像色彩空间。

**语法：**

```
*bool* Imagick::setImageColorspace( *int* $colorspace )
```

**参数：**此函数接受单个参数**$colorspace**，该参数保存与[个颜色空间常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.colorspace-undefined)之一相对应的整数值。

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

下面的程序演示了 PHP 中的**Imagick：：setImageColorspace()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the image colorspace
$imagick->setImageColorspace(imagick::COLORSPACE_RGB);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/782c90925bc0aae1dbc9c85c0ab4ecb0.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the image colorspace
$imagick->setImageColorspace(imagick::COLORSPACE_OHTA);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/71a17554020af23325ef7c10a892e705.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagecolorspace.php](https://www.php.net/manual/en/imagick.setimagecolorspace.php)