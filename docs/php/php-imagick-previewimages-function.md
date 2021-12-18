# PHP|Imagick previewImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-previewimages-function/](https://www.geeksforgeeks.org/php-imagick-previewimages-function/)

**Imagick：：previewImages()函数**是 PHP 中的一个内置函数，用于快速定位图像处理的适当参数。 它平铺指定图像的 9 个缩略图，并以不同的强度应用图像处理操作。

**语法：**

```php
*bool* Imagick::previewImages( *int* $preview )
```

**参数：**此函数接受保存预览类型常量的单个参数**$PREVIEW**。 [单击此处](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.preview-undefined)获取预览类型常量列表。

**返回值：**此函数成功时返回 TRUE，错误或失败时返回 FALSE。

**错误/异常：**发生错误时抛出 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：previewImages()函数：

**程序：**

```php
<?php 

// Store the image source into variable
$imagePath =
"https://cdncontribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png";

// Create new Imagick object
$imagick = new \Imagick($imagePath);

// Use previewImages() function
$imagick->previewImages(imagick::PREVIEW_EDGEDETECT);

header("Content-Type: image/png");

// Display output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/ce79e6e877cd2cd5fcf431da88301f1a.png)

**引用：**[https://www.php.net/manual/en/imagick.previewimages.php](https://www.php.net/manual/en/imagick.previewimages.php)