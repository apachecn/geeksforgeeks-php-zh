# PHP|imagepng()函数

> Original: [https://www.geeksforgeeks.org/php-imagepng-function/](https://www.geeksforgeeks.org/php-imagepng-function/)

函数**imagepng()**是 PHP 中的一个内置函数，用于将图像显示到浏览器或文件。 此函数的主要用途是在浏览器中查看图像、将任何其他图像类型转换为 PNG 以及对图像应用滤镜。

**语法：**

```php
*bool* imagepng( *resource* $image, *int* $to, *int* $quality, *int* $filters)
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$to(可选)：**它指定保存文件的路径。
*   **$quality(可选)：**它指定图像的质量。
*   **$Filters(可选)：**它指定要应用于图像的滤镜，这些滤镜有助于减小图像大小。

**返回值：**此函数成功时返回 TRUE，错误时返回 FALSE。

下面的示例说明了 PHP 中的**imagepng()函数**：

**示例 1：**在此示例中，我们将在浏览器中查看图像。

## PHP

```php
<?php

// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// View the loaded image in browser using imagepng() function
header('Content-type: image/png');  
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**示例 2：**在此示例中，我们将 JPEG 转换为 PNG。

## PHP

```php
<?php

// Load an image from JPEG URL
$im = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert the image into PNG using imagepng() function
imagepng($im, 'converted.png');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the PNG version of image in the same folder where your PHP script is.
```

**程序 3：**在本例中，我们将使用过滤器。

## PHP

```php
<?php

// Create an image instance
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Save the image as image1.png
imagepng($im, 'image1.png');

// Save the image as image2.png with all filters to disable size compression
imagepng($im, 'image2.png', null, PNG_ALL_FILTERS);

imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the image1.png as compressed and image2.png as uncompressed image
```

![](img/1ace09e1be62a426d02335e079baa84f.png)

**引用：**[https://www.php.net/manual/en/function.imagepng.php](https://www.php.net/manual/en/function.imagepng.php)