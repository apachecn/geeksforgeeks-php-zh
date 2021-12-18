# PHP|Imagick AdaptiveSharpenImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-adaptivesharpenimage-function/](https://www.geeksforgeeks.org/php-imagick-adaptivesharpenimage-function/)

**Imagick：：AdaptiveSharpenImage()**函数是 PHP 中的一个内置函数，它为图像提供自适应锐化图像功能。 自适应锐化图像的强度取决于图像边缘的显著减少。

**语法：**

```php
*bool* Imagick::adaptiveSharpenImage ( $radius, $sigma, $channel )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Radius：**此参数用于设置高斯半径(以像素为单位)。 它不包括中心像素。 如果半径值为零，则表示将自动选择半径。
*   **$sigma：**此参数用于查找高斯的标准偏差(以像素为单位)。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道是 Imagick：：Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：AdaptiveSharpenImage()**函数：

**原始图像：**
![original image link](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序：**

```php
<?php

// require_once('path/to/vendor/autoload.php');

header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$image->adaptiveSharpenImage(19, 8);
echo $image;
?>
```

**输出：**
![adaptive sharpen image](img/c71265c354c43b516ec487e3f2a7b5a2.png)

**引用：**[http://php.net/manual/en/imagick.adaptivesharpenimage.php](http://php.net/manual/en/imagick.adaptivesharpenimage.php)