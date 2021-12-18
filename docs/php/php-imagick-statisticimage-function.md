# PHP|Imagick statticImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-statisticimage-function/](https://www.geeksforgeeks.org/php-imagick-statisticimage-function/)

**Imagick：：Statistics ticImage()**函数是 PHP 中的一个内置函数，用于用指定宽度和高度附近的相应统计数据替换每个像素。

**语法：**

```php
*bool* Imagick::statisticImage( $type, $width, $height, $channel )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$type：**该参数用于设置图片的统计类型。
*   **$width：**此参数设置图像的像素宽度。
*   **$Height：**此参数设置图像的像素高度。
*   **$channel：**此参数用于设置通道。 Channel 的默认值为 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：Statistics ticImage()**函数：

**程序：**

```php
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use statisticImage function
$imagick->statisticImage(10, 5,    5);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![statistics image](img/7a61397364fa9bee68525bca409311a3.png)

**相关文章：**

*   [PHP|Imagick getImageColors()函数](https://www.geeksforgeeks.org/php-imagick-getimagecolors-function/)
*   [PHP|Imagick choImage()函数](https://www.geeksforgeeks.org/php-imagick-chopimage-function/)
*   [PHP|Imagick VignetteImage()函数](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)

**引用：**[http://php.net/manual/en/imagick.statisticimage.php](http://php.net/manual/en/imagick.statisticimage.php)