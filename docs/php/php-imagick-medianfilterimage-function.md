# PHP|Imagick medianFilterImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-medianfilterimage-function/](https://www.geeksforgeeks.org/php-imagick-medianfilterimage-function/)

**Imagick：：medianFilterImage()函数**是 PHP 中的一个内置函数，它应用数字过滤器来改善噪声图像的质量。

**语法：**

```php
*bool* Imagick::medianFilterImage( *float* $radius )
```

**参数：**该函数接受单个参数**$Radius**，该参数保存像素邻域的半径。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时抛出 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：medianFilterImage()函数：

**程序：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Applying the digital filter to the image
$imagick->medianFilterImage(10);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/51e30f27f222b275ff4e3a1e47d3a7a3.png)

**引用：**[https://www.php.net/manual/en/imagick.medianfilterimage.php](https://www.php.net/manual/en/imagick.medianfilterimage.php)