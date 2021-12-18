# PHP|imagewebp()函数

> Original: [https://www.geeksforgeeks.org/php-imagewebp-function/](https://www.geeksforgeeks.org/php-imagewebp-function/)

函数**imagewebp()**是 PHP 的内置函数，用于将图像显示到浏览器或文件。 此功能的主要用途是在浏览器中查看图像、将任何其他图像类型转换为 WebP 以及更改图像质量。
**语法：**

```php
*bool* imagewebp( *resource* $image, *int* $to, *int* $quality)

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$to(可选)：**它指定保存文件的路径。
*   **$quality(可选)：**它指定图像的质量。

**返回值：**此函数成功时返回 TRUE，错误时返回 FALSE。
以下示例说明 PHP 中的**imagewebp()函数**：
**示例 1：**在此示例中，我们将在浏览器中查看图像。

## PHP

```php
<?php

// Load an image from local webp file
// Images can be converted into webp 
// using imagewebp() function or other
// online convertors
$im = imagecreatefromwebp('./geeksforgeeks.webp');

// View the loaded image in browser
// using imagewebp() function
header('Content-type: image/webp');  
imagewebp($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**示例 2：**在此示例中，我们将 PNG 转换为 WebP。

## PHP

```php
<?php

// Load an image from local webp file
// Images can be converted into webp 
// using imagewebp() function or other
// online convertors
$im = imagecreatefromwebp('./geeksforgeeks.webp');

// Convert the image into webp
// using imagewebp() function
imagewebp($im, 'converted.webp');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the WEBP version of image in the same folder where your PHP script is.

```

**程序 3：**在本例中，我们将更改图像质量。

## PHP

```php
<?php

// Load an image from local webp file
// Images can be converted into webp 
// using imagewebp() function or other
// online convertors
$im = imagecreatefromwebp('./geeksforgeeks.webp');

// Convert the image into webp using imagewebp()
// function and view in the browser
header('Content-type: image/webp');
imagewebp($im, null, 0);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/c7b6949fa65776582799a765e567de0f.png)

**引用：**[https://www.php.net/manual/en/function.imagewebp.php](https://www.php.net/manual/en/function.imagewebp.php)