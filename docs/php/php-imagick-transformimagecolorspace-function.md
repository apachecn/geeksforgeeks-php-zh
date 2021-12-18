# PHP|Imagick 转换 ImageColorspace()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-transformimagecolorspace-function/](https://www.geeksforgeeks.org/php-imagick-transformimagecolorspace-function/)

**Imagick：：TransImageColorspace()**函数是 PHP 中的一个内置函数，用于将图像转换为新的色彩空间。

**语法：**

```
*bool* Imagick::transformImageColorspace( $colorspace )
```

**参数：**此函数接受用于转换彩色图像的单个参数*$Colorspace*。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：TransImageColorspace()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Transform the image in RGB color space
$imagick->transformimagecolorspace('RGB');

// Separate the image channel
$imagick->separateImageChannel(1);
header("Content-Type: image/jpg");

// Display the output Image
echo $imagick->getImageBlob();
?>
```

**输出：**
![transform image color space](img/f6d4f6bc736a00ae71c16be24e8e4dc0.png)

**相关文章：**

*   [PHP|Imagick autoLevelImage()函数](https://www.geeksforgeeks.org/php-imagick-autolevelimage-function/)
*   [PHP|Imagick addNoiseImage()函数](https://www.geeksforgeeks.org/php-imagickaddnoiseimage-function/)

**引用：**[http://php.net/manual/en/imagick.transformimagecolorspace.php](http://php.net/manual/en/imagick.transformimagecolorspace.php)