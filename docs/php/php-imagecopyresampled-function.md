# PHP|imagecopyressamed()函数

> Original: [https://www.geeksforgeeks.org/php-imagecopyresampled-function/](https://www.geeksforgeeks.org/php-imagecopyresampled-function/)

**imagecopyressamed()函数**是 PHP 中的一个内置函数，用于将一个图像的矩形部分复制到另一个图像，平滑地内插像素值，以便特别是减小图像大小时仍能保持很大的清晰度。

**语法：**

> *bool*图像复制采样(*资源*$dst_image，*资源*$src_image，*int*$dst_x，*int*$dst_y，*int*$src_x，*int*$src_y，*int*$dst。 *int*$src_h)

**参数：**此函数接受上述 10 个参数，如下所述：

*   **$dst_image：**它指定目标图像资源。
*   **$src_image：**它指定源图像资源。
*   **$dst_x：**它指定目标点的 x 坐标。
*   **$dst_y：**它指定目标点的 y 坐标。
*   **$src_x：**它指定源点的 x 坐标。
*   **$src_y：**它指定源点的 y 坐标。
*   **$dst_w：**它指定目标宽度。
*   **$dst_h：**它指定目标高度。
*   **$src_w：**它指定源宽度。
*   **$src_h：**它指定震源高度。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**imagecopyressamed()函数**：
**程序 1(将图像重新采样为其宽度和高度的一半)：**

```
<?php
// Get dimensions of new image
list($width, $height) = getimagesize(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// Reduce width and height to half
$new_width = $width * 0.5;
$new_height = $height * 0.5;

// Resample the image
$image_p = imagecreatetruecolor($new_width, $new_height);
$image = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $new_width, $new_height, $width, $height);

// Output the image to browser
header('Content-Type: image/jpeg');
imagejpeg($image_p, null, 100);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/903458335de6316607072b1e5e36f418.png)

**程序 2(使用固定宽度和高度重采样图像)：**

```
<?php
// Set a  fixed height and width
$width = 300;
$height = 300;

// Get image dimensions
list($width_orig, $height_orig) = getimagesize(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// Resample the image
$image_p = imagecreatetruecolor($width, $height);
$image = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $width, $height, $width_orig, $height_orig);

// Output the image
header('Content-Type: image/jpeg');
imagejpeg($image_p, null, 100);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/76560caa3e982e7c288436572476dabd.png)

**引用：**[https://www.php.net/manual/en/function.imagecopyresampled.php](https://www.php.net/manual/en/function.imagecopyresampled.php)