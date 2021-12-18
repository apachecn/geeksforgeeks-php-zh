# PHP|Imagick cropThumbnailImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-cropthumbnailimage-function/](https://www.geeksforgeeks.org/php-imagick-cropthumbnailimage-function/)

Imagick：：cropThumbnailImage()函数是 PHP 中的内置函数，用于创建裁剪的缩略图。 此函数通过首先使用高度和权重参数放大或缩小图像，然后从图像中心裁剪区域来创建固定大小的缩略图。

**注意：**在使用.gif 图像格式时，使用 cropThumbnailImage()函数可能会产生不需要的结果。 如果您使用的是.gif，则需要通过删除画布来补充此功能。

**语法：**

```
*bool* Imagick::cropThumbnailImage( $width, $height, $legacy = FALSE )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$width：**此参数保存缩略图的宽度。
*   **$Height：**此参数保存缩略图的高度。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

**原始图像：**
![](img/176c5f6b65db3617c36d78213273e7a2.png)

下面的程序演示了 PHP 中的 Imagick：：cropThumbnailImage()函数：

**程序：**

```
<?php

// Create a new object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190714133012/gfg390x152.png');

// Crop and resize the image
$image -> cropThumbnailImage(300, 50);

// Remove the canvas using the line below 
// if the image is a .gif file:
// $image->setImagePage(0, 0, 0, 0);

// Image header
header('Content-type: image/png');

// Display resulting image:
echo $image;

?>
```

**输出：**
![](img/3b514fd5c996359993fe040761a60f45.png)

**引用：**[https://www.php.net/manual/en/imagick.cropthumbnailimage.php](https://www.php.net/manual/en/imagick.cropthumbnailimage.php)