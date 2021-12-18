# PHP|Imagick clutImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-clutimage-function/](https://www.geeksforgeeks.org/php-imagick-clutimage-function/)

Imagick：：clutImage()函数是 PHP 中的一个内置函数，用于替换图像中的颜色。 此函数的第二个参数替换特定通道中的颜色。

**语法：**

```
*bool* Imagick::clutImage( $lookup_table, $channel = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$LOOKUP_TABLE：**此参数包含颜色查找表的 Imagick 对象。
*   **$channel：**它是提供对您的通道模式有效的任何通道的通道常量。 $channel 的默认值为 Imagick：：Channel_Default。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 Imagick：：clutImage()函数：

**程序：**

## PHP

```
<?php

// Declare an Imagick object
$image = new Imagick(
'https://write.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png');

$clut = new Imagick();

// Imagick object chosen green color from color lookup table
$clut->newImage(1, 1, new ImagickPixel('green'));

// No channel is applied hence default channel is used
$image->clutImage($clut);

header("Content-Type: image/jpg");

// Display the output image
echo $image->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/a24fcf475a551320c1998efddffbb5be.png)

**引用：**[https://www.php.net/manual/en/imagick.clutimage.php](https://www.php.net/manual/en/imagick.clutimage.php)