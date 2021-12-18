# PHP|Imagick AdaptiveBlurImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/](https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/)

**Imagick：：AdaptiveBlurImage()**函数是 PHP 中的内置函数，用于在给定图像中添加自适应模糊滤镜。 自适应模糊的强度在图像边缘显著降低，而标准模糊在整个图像上是均匀的。 这种效果会使图像不清晰或不清晰。

**语法：**

```php
*bool* adaptiveBlurImage ( $radius, $sigma, $channel )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Radius：**此参数用于设置高斯半径(以像素为单位)。 它不包括中心像素。 如果半径值为零，则表示将自动选择半径。
*   **$sigma：**此参数用于查找高斯的标准偏差(以像素为单位)。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道为**Imagick：：Channel_Default**。
    频道列表的一些颜色常数如下：
    *   Imagick：：COLOR_BLACK(整数)
    *   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
    *   Imagick：：color_cyan(整数)
    *   Imagick：：COLOR_GREEN(整数)
    *   Imagick：：COLOR_RED(整数)
    *   Imagick：：COLOR_ 黄色(整数)
    *   Image：：COLOR_MAGIC(整数)
    *   Imagick：：color_opacity(整数)
    *   Imagick：：COLOR_Alpha(整数)
    *   加入时间：清华大学 2007 年 01 月 25 日下午 3：33

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：AdaptiveBlurImage()**函数：

**原始图像：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序：**

```php
<?php 
// require_once('path/to/vendor/autoload.php'); 
header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$image->adaptiveBlurImage(20, 5);

echo $image;
?>
```

**输出：**
![blur image](img/3a3e8e3664f0ed27ccff99f8f378b30e.png)

**引用：**[http://php.net/manual/en/imagick.adaptiveblurimage.php](http://php.net/manual/en/imagick.adaptiveblurimage.php)