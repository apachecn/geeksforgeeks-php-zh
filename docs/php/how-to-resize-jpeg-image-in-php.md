# 如何在 PHP 中调整 JPEG 图像的大小？

> 原文:[https://www . geesforgeks . org/如何调整大小-jpeg-image-in-php/](https://www.geeksforgeeks.org/how-to-resize-jpeg-image-in-php/)

**为什么我们需要调整图像的大小？**
在网站中，我们经常需要缩放图像以适合特定的部分。有时，有必要缩小任意大小的图像，以适合封面照片部分或个人资料图片部分。此外，我们需要显示一个更大图像的缩略图。在这些情况下，总是手动调整图像大小是不可行的。

解决上述问题的一种方法是使用以下方法，我们只需要在 HTML 中设置图像标签的宽度和高度属性。

```
<img src="check.jpg" height="100" width="100" alt="Image resize">
```

这样做的问题是，整个图像都是从服务器下载的，并且在浏览器中以减小的尺寸显示。这意味着需要相同数量的带宽来以较小的尺寸显示图像，这在原始尺寸的情况下是需要的。

**使用 PHP 在服务器端调整图像大小:**我们以后将使用 PHP 来减少图像尺寸并渲染它，以便较小的尺寸仅在客户端下载，而不是原始图像。为了实现这一点，我们将使用 PHP 中的 **[imagecopyresampled()函数](https://www.geeksforgeeks.org/php-imagecopyresampled-function/)** 。

[image copyresholded()函数](https://www.geeksforgeeks.org/php-imagecopyresampled-function/)用于通过重采样来复制图像或图像的一部分并调整其大小。

**语法:**

```
*bool* imagecopyresampled( *resource* $dst_image, *resource* $src_image,
                  *int* $dst_x, *int* $dst_y, *int* $src_x, *int* $src_y,
                  *int* $dst_w, *int* $dst_h, *int* $src_w, *int* $src_h )
```

**参数:**该功能从位置 *($src_x，$src_y)* 处的宽度 *$src_w* 和高度 *$src_h* 的 *$src_image* 中接受一个矩形区域，并将其放置在宽度 *$dst_w* 和高度 *$dst_h* 处的 *$dst_image* 的矩形区域中

**示例:**本示例使用 imagecopyresampled()函数调整图像大小。

```
<?php

// The file concerned
$filename = 'check.jpg';

// Maximum width and height
$width = 100;
$height = 100;

// File type
header('Content-Type: image/jpg');

// Get new dimensions
list($width_orig, $height_orig) = getimagesize($filename);

$ratio_orig = $width_orig/$height_orig;

if ($width/$height > $ratio_orig) {
    $width = $height*$ratio_orig;
} else {
    $height = $width/$ratio_orig;
}

// Resampling the image 
$image_p = imagecreatetruecolor($width, $height);
$image = imagecreatefromjpeg($filename);

imagecopyresampled($image_p, $image, 0, 0, 0, 0,
        $width, $height, $width_orig, $height_orig);

// Display of output image
imagejpeg($image_p, null, 100);

?>
```

**输出:**

*   **原图:**
    ![Original image](img/752422974896acbbdf90ec5e7f03ffff.png)
*   **输出图像:**
    ![Final image](img/b3da27d84132f3832645255e505579c5.png)