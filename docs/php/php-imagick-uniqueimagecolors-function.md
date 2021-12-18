# PHP|Imagick Unique eImageColors()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-uniqueimagecolors-function/](https://www.geeksforgeeks.org/php-imagick-uniqueimagecolors-function/)

**Imagick：：Unique eImageColors()**函数是 PHP 中的一个内置函数，用于丢弃任何像素颜色中除一种以外的所有颜色。 此功能在版本 6.2.9 或更高版本中可用。

**语法：**

```
*bool* Imagick::uniqueImageColors( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：Unique eImageColors()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Reduce the image to 256 colours nicely.
$imagick->quantizeImage(256, \Imagick::COLORSPACE_YIQ, 0, false, false);

// Use uniqueImageColors function to distinguish the color of image
$imagick->uniqueImageColors();

// Scale the output image
$imagick->scaleimage($imagick->getImageWidth() * 10, 
              $imagick->getImageHeight() * 50);
header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![unique image colors](img/c1c8f5cc6f45e6309d10d5d9d489efc0.png)

**相关文章：**

*   [PHP|Imagick autoLevelImage()函数](https://www.geeksforgeeks.org/php-imagick-autolevelimage-function/)
*   [PHP|Imagick borderImage()函数](https://www.geeksforgeeks.org/php-imagick-borderimage-function/)

**引用：**[http://php.net/manual/en/imagick.uniqueimagecolors.php](http://php.net/manual/en/imagick.uniqueimagecolors.php)