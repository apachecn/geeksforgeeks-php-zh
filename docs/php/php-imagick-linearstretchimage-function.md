# PHP|Imagick linearStretchImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-linearstretchimage-function/](https://www.geeksforgeeks.org/php-imagick-linearstretchimage-function/)

**Imagick：：linearStretchImage()函数**是 PHP 中的一个内置函数，用于在饱和的情况下拉伸图像强度。 Imagick：：linearStretchImage()函数的计算以像素倍数为单位，同时带有黑点和白点。

**语法：**

```
*bool* Imagick::linearStretchImage( $blackPoint, $whitePoint )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$BLACKPOINT：**此参数保存图像黑点。
*   **$WhitePoint：**此参数保存图像白点。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的 Imagick：：linearStretchImage()函数：

**程序：**此程序使用 Imagick：：linearStretchImage()函数以饱和度拉伸图像强度。

```
<?php

// Store the image into variable
$imagePath=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png";

// Store the value of variables
$blackThreshold = 23;
$whiteThreshold = 45;

// Declare new Imagick object
$imagick = new \Imagick($imagePath);

// Calculate the pixels of image
$pixels = $imagick->getImageWidth() * $imagick->getImageHeight();

// Use linearStretchImage() function to stretches with
// saturation the image intensity
$imagick->linearStretchImage($blackThreshold * $pixels, $whiteThreshold * $pixels);

header("Content-Type: image/jpeg");

// Display the image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/eeaae880c638d3d6f98119f395fdd87d.png)

**引用：**[https://www.php.net/manual/en/imagick.linearstretchimage.php](https://www.php.net/manual/en/imagick.linearstretchimage.php)