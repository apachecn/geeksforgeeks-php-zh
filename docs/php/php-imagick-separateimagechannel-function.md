# PHP|Imagick parateImageChannel()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-separateimagechannel-function/](https://www.geeksforgeeks.org/php-imagick-separateimagechannel-function/)

**Imagick：：SeparateImageChannel()函数**是 PHP 中的一个内置函数，用于将通道从图像中分离出来，并返回灰度图像。 通道是图像中每个像素的特定颜色分量。

**语法：**

```
*bool* Imagick::separateImageChannel( *int* $channel )
```

**参数：**此函数接受单个参数**$channel**，该参数保存与通道常量之一相对应的整数值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：SeparateImageChannel()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Separate the image channel
$imagick->separateImageChannel(1);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/12bd74e96c93e24d9f49db75de095500.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Apply selectiveBlurImage() function
$imagick->separateImageChannel(imagick::CHANNEL_GREEN);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/b545c096d4f3c0a06a12c90e1fd21e4d.png)

**引用：**[https://www.php.net/manual/en/imagick.separateimagechannel.php](https://www.php.net/manual/en/imagick.separateimagechannel.php)