# PHP|imagefilter()函数

> Original: [https://www.geeksforgeeks.org/php-imagefilter-function/](https://www.geeksforgeeks.org/php-imagefilter-function/)

**imagefilter()函数**是 PHP 中的一个内置函数，用于对图像应用给定的滤镜。

**语法：**

```php
*bool* imagefilter( *resource* $image, *int* $filtertype,
       *int* $arg1, *int* $arg2, *int* $arg3, *int* $arg4 )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$image：**它指定要处理的图像。
*   **$filtertype：**它指定要使用的过滤器，该过滤器是一个整数，对应于[img_filter 常量](https://www.php.net/manual/en/image.constants.php#constant.img-filter-negate)
    所有 img_filter 常量的列表如下：
    *   **img_filter_Negate(0)：**反转图像的所有颜色。
    *   **img_filter_grayscale(1)：**通过将红色、绿色和蓝色分量更改为其加权和，将图像转换为灰度。
    *   **img_filter_brightness(2)：**更改图像的亮度。 使用**$arg1**设置亮度级别。 亮度的范围是-255 到 255。
    *   **img_filter_contrast(3)：**更改图像的对比度。 使用**$arg1**设置对比度级别。
    *   **img_filter_Colorize(4)：**喜欢 img_filter_grayscale，除非您可以指定颜色。 使用红、绿、蓝和 arg4 形式的**$arg1**、**$arg2**和**$arg3**作为 Alpha 通道。 每种颜色的范围是 0 到 255。
    *   **IMG_FILTER_EDGEDETECT(5)：**使用边缘检测来突出显示图像中的边缘。
    *   **img_filter_uss_blur(6)：**将高斯模糊应用于图像。
    *   **img_filter_selectional_blur(7)：**将选择性模糊应用于图像。
    *   **img_filter_emoss(8)：**将浮雕应用于图像。
    *   **IMG_FILTER_Mean_Removal(9)：**从图像中去除噪点，并给人‘粗略’的效果。
    *   **img_filter_Smooth(10)：**使图像更平滑。 使用**$arg1**设置平滑度。
    *   **img_filter_Pixelate(11)：**对图像应用像素化效果，使用**$arg1**设置块大小，使用**$arg2**设置像素化效果模式。
    *   **img_filter_discatter(12)：**对图像应用散射效果，使用**$arg1**和**$arg2**定义效果强度，另外使用**$arg3**仅应用选定像素颜色。
*   **$arg1(可选)：**它指定第一个参数。
*   **$arg2(可选)：**它指定第二个参数。
*   **$arg3(可选)：**它指定第三个参数。
*   **$arg4(可选)：**它指定第四个参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**imagefilter()函数**：

**程序 1：**

```php
<?php

// Load the png image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Negative the image
imagefilter($im, IMG_FILTER_NEGATE);

// Show the output
header('Content-type: image/png');
imagepng($im);
?>
```

**输出：**
![](img/70089d12301237a2b49fc5db48164343.png)

**程序 2：**

```php
<?php

// Load the png image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Grayscale the image
imagefilter($im, IMG_FILTER_GRAYSCALE);

// Show the output
header('Content-type: image/png');
imagepng($im);
?>
```

**输出：**
![](img/a09a5e363ad65bc8fe648b04bb282940.png)

**程序 3：**

```php
<?php

// Load the png image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Colorize the image
imagefilter($im, IMG_FILTER_COLORIZE, 140, 0, 140, 20);

// Show the output
header('Content-type: image/png');
imagepng($im);
?>
```

**输出：**
![](img/ee843f2019128193d391df0b05dc9a9e.png)

**引用：**[https://www.php.net/manual/en/function.imagefilter.php](https://www.php.net/manual/en/function.imagefilter.php)