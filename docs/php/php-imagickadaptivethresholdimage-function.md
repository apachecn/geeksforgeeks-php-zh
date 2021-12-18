# PHP|Imagick AdaptiveThresholdImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagickadaptivethresholdimage-function/](https://www.geeksforgeeks.org/php-imagickadaptivethresholdimage-function/)

**Imagick：：AdaptiveThresholdImage()**函数是 PHP 中的一个内置函数，用于根据每个像素的局部邻域中的强度值为其选择阈值。 此函数允许对全局强度直方图不包含明显峰值的图像进行阈值处理。

**语法：**

```php
*bool* Imagick::adaptiveThresholdImage ( $width, $height, $offset )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$width：**该参数用于设置本地邻域的宽度。
*   **$Height：**此参数用于设置本地邻域的高度。
*   **$Offset：**此参数用于设置平均偏移量。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：AdaptiveThresholdImage()**函数：

**原始图像：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序：**

```php
<?php

// require_once('path/to/vendor/autoload.php'); 

header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$image->adaptiveThresholdImage(1024, 73, 0.625);

echo $image;
?>
```

**输出：**
![adaptive thresold image](img/92655fac130f4772488bfafcfb48fc6d.png)

**引用：**[http://php.net/manual/en/imagick.adaptivethresholdimage.php](http://php.net/manual/en/imagick.adaptivethresholdimage.php)