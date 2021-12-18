# PHP|Imagick ThresholdImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-thresholdimage-function/](https://www.geeksforgeeks.org/php-imagick-thresholdimage-function/)

**Imagick：：ThresholdImage()**函数是 PHP 中的一个内置函数，用于根据阈值更改单个像素的值。

**语法：**

```php
*bool* Imagick::thresholdImage( $threshold, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Threshold：**此参数设置阈值。
*   **$channel：**此参数设置图像的通道。 CHANNEL_DEFAULT 用作默认通道。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：ThresholdImage()**函数：

**程序：**

```php
<?php

// Create an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use thresholdimage function
$imagick->thresholdimage(0.5, 2);
header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![thresholdimage](img/1e7771e358ab51105c9b732cb8696bce.png)

**相关文章：**

*   [PHP|Imagick AdaptiveSharpenImage()函数](https://www.geeksforgeeks.org/php-imagick-adaptivesharpenimage-function/)
*   [PHP|Imagick AdaptiveBlurImage()函数](https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/)

**引用：**[http://php.net/manual/en/imagick.thresholdimage.php](http://php.net/manual/en/imagick.thresholdimage.php)