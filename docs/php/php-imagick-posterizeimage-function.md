# PHP|Imagick AfterizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-posterizeimage-function/](https://www.geeksforgeeks.org/php-imagick-posterizeimage-function/)

**Imagick：：AfterizeImage()**函数是 PHP 中的一个内置函数，用于将图像减少到有限的颜色级别。

**语法：**

```
*bool* Imagick::posterizeImage( $levels, $dither )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Levels：**此参数用于设置颜色级别。
*   **$dither：**此参数用于保存抖动布尔值。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：AfterizeImage()**函数：

**程序：**

```
<?php

// Create an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use posterizeImage function
$imagick->posterizeImage(8, 'true');

// Set image format
$imagick->setImageFormat('png');

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![posterize image](img/e437a8442a4aac40a90689696eb26ea2.png)

**引用：**[http://php.net/manual/en/imagick.posterizeimage.php](http://php.net/manual/en/imagick.posterizeimage.php)