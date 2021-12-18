# PHP|Imagick pliceImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-spliceimage-function/](https://www.geeksforgeeks.org/php-imagick-spliceimage-function/)

**Imagick：：SpliceImage()**函数是 PHP 中的一个内置函数，用于将纯色拼接到图像中。

**语法：**

```php
*bool* Imagick::spliceImage( $width, $height, $x, $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width：**该参数用于设置图片的切片宽度。
*   **$Height：**此参数用于设置图像的切片高度。
*   **$x：**此参数用于设置 x 轴上的切片位置。
*   **$y：**此参数用于设置 y 轴上的切片位置。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：SpliceImage()**函数：

**程序：**

```php
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use spliceImage function
$imagick->spliceImage(50, 100, 50, 100);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![splice image](img/f587d6171aa1b8fb8e0108359a6e8b08.png)

**相关文章：**

*   [PHP|Imagick choImage()函数](https://www.geeksforgeeks.org/php-imagick-chopimage-function/)
*   [PHP|Imagick VignetteImage()函数](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)

**引用：**[http://php.net/manual/en/imagick.spliceimage.php](http://php.net/manual/en/imagick.spliceimage.php)