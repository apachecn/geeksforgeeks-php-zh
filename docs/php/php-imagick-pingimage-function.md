# PHP|Imagick pingImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-pingimage-function/](https://www.geeksforgeeks.org/php-imagick-pingimage-function/)

**Imagick：：pingImage()函数**是 PHP 中的一个内置函数，用于获取图像的基本属性。 此方法用于查询图像的宽度、高度、大小和格式，而无需将整个图像读取到内存中。

**语法：**

```php
*bool* Imagick::pingImage( $filename )

```

**参数：**此函数接受单个参数**$filename**，该参数保存图像的文件名。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的 Imagick：：pingImage()函数：

**程序：**该程序通过图像链接告诉图像的高度和宽度。

```php
<?php

// Create new Imagick object
$image = new Imagick();

// Use Imagick::pingImage() function to the image
$image->pingImage(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Use getImageWidth() function to for image width attribute
$width = $image->getImageWidth();

// Use getImageHeight() function to for image width attribute
$height = $image->getImageHeight();

// Display the output
echo "Width of image: " . $width . "px<br>";
echo "Height of image: " . $height . "px";

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.pingimage.php](https://www.php.net/manual/en/imagick.pingimage.php)