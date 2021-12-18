# PHP|Imagick NormizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-normalizeimage-function/](https://www.geeksforgeeks.org/php-imagick-normalizeimage-function/)

**Imagick：：NormizeImage()**函数是 PHP 中的一个内置函数，用于通过调整像素的颜色来增强彩色图像的对比度，以覆盖整个可用的颜色范围。

**语法：**

```php
*bool* Imagick::normalizeImage( $channel )
```

**参数：**此函数接受单个参数*$channel*。 此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道为**Imagick：：Channel_Default。**

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：NormizeImage()**函数：

**程序：**

```php
<?php

// Create an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Create a copy image
$original = clone $imagick;

// Set the width and height of image
$original->cropimage($original->getImageWidth() / 2,
                 $original->getImageHeight(), 0, 0);

// Use normalizeImage function
$imagick->normalizeImage();

// Use compositeimage function
$imagick->compositeimage($original, \Imagick::COMPOSITE_ATOP, 0, 0);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![normalize image](img/83e74791b3e56afae5ab514ba012e0e9.png)

**引用：**[http://php.net/manual/en/imagick.normalizeimage.php](http://php.net/manual/en/imagick.normalizeimage.php)