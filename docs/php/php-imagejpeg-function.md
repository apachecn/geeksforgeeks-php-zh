# PHP|imagejpeg()函数

> Original: [https://www.geeksforgeeks.org/php-imagejpeg-function/](https://www.geeksforgeeks.org/php-imagejpeg-function/)

函数的作用是：**imagejpeg()函数**是 PHP 的内置函数，用于将图像显示到浏览器或文件。 此功能的主要用途是在浏览器中查看图像、将任何其他图像类型转换为 JPEG 以及更改图像质量。

**语法：**

```php
*bool* imagejpeg( *resource* $image, *int* $to, *int* $quality )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$to(可选)：**它指定保存文件的路径。
*   **$quality(可选)：**它指定图像的质量。

**返回值：**此函数成功时返回 TRUE，错误时返回 FALSE。

下面的示例说明了 PHP 中的**imagejpeg()函数**：

**示例 1：**在此示例中，我们将在浏览器中查看图像。

```php
<?php

// Load an image from jpeg URL
$im = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// View the loaded image in browser using imagejpeg() function
header('Content-type: image/jpg');  
imagejpeg($im);
imagedestroy($im);
?>
```

**输出：**
![](img/64dd68eb9092c0cee9aa5d7f65d4a2d0.png)

**示例 2：**在本例中，我们将 PNG 转换为 JPEG。

```php
<?php

// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert the image into JPEG using imagejpeg() function
imagejpeg($im, 'converted.jpg');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the JPEG version of image
in the same folder where your PHP script is.

```

**示例 3：**在此示例中，我们将更改图像质量。

```php
<?php

// Load an image from jpeg URL
$im = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// View the loaded image in browser using imagejpeg() function
header('Content-type: image/jpg');  
// Decrease the quality of image to 2
imagejpeg($im, null, 2);
imagedestroy($im);
?>
```

**输出：**
![](img/d4c90d579dfd881efddb872eae919a44.png)

**引用：**[https://www.php.net/manual/en/function.imagejpeg.php](https://www.php.net/manual/en/function.imagejpeg.php)