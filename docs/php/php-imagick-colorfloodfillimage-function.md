# PHP|Imagick ColorFlodfulImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-colorfloodfillimage-function/](https://www.geeksforgeeks.org/php-imagick-colorfloodfillimage-function/)

Imagick：：ColorFlodfulImage()函数是 PHP 中的一个内置函数，用于更改与目标匹配的任何像素的颜色值。

**语法：**

```php
*bool* Imagick::colorFloodfillImage( $color, $fuzz, $bordercolor, $x, $y )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **color：**此参数保存 ImagickPixel 对象，该对象包含字符串格式的填充颜色名称。
*   **fuzz：**此参数保存模糊量。
*   **borderColor：**此参数保存 ImagickPixel 对象，该对象包含字符串格式的填充边框颜色名称。
*   **x：**它保持填方体的 x 轴起始位置。
*   **y：**它保持填方体的 y 轴起始位置。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

**程序：**

```php
<?php

// Create an Imagick object
$image = new Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png");

// Use colorFloodfillImage() function to change
// the color value of any pixel
$image->colorFloodfillImage( "red", 0.2, "white", 1, 1);

header("Content-Type: image/jpg");

// Display the output
echo $image->getImageBlob();
?>
```

**输出：**
![](img/6396bdbd61d09ec5f4fea53609011337.png)

**引用：**[https://www.php.net/manual/en/imagick.colorfloodfillimage.php](https://www.php.net/manual/en/imagick.colorfloodfillimage.php)