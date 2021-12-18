# PHP|imagexbm()函数

> Original: [https://www.geeksforgeeks.org/php-imagexbm-function/](https://www.geeksforgeeks.org/php-imagexbm-function/)

函数的作用是：**imagexbm()函数**是 PHP 中的一个内置函数，用于将图像显示到浏览器中的文件。 此函数的主要用途是在浏览器中查看图像，并将任何其他图像类型转换为 XBM。

**语法：**

```php
*bool* imagexbm( *resource* $image, *int* $to, *int* $foreground)
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$image:** it specifies the image resources to be processed.
*   **$to (optional):** it specifies the path where the file is saved.
*   **$forecround (optional):** specifies the foreground of the image.

**返回值：**此函数成功时返回 TRUE，错误时返回 FALSE。

下面的示例说明了 PHP 中的**imagexbm()函数**：

**示例 1：**在此示例中，我们将在浏览器中下载图像。

```php
<?php

// Load an xbm image from local folder
// Image can be converted into xbm using
// online convertors or imagexbm()
$im = imagecreatefromxbm('geeksforgeeks.xbm');

// Download the image
header('Content-Type: image/xbm');
imagexbm($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在本例中，我们将 PNG 转换为 XBM。

```php
<?php

// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert the image into XBM using imagexbm() function
imagexbm($im, 'converted.xbm');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagexbm.php](https://www.php.net/manual/en/function.imagexbm.php)