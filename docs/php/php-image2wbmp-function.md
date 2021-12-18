# PHP|image2wbmp()函数

> Original: [https://www.geeksforgeeks.org/php-image2wbmp-function/](https://www.geeksforgeeks.org/php-image2wbmp-function/)

函数的作用是：**image2wbmp()函数**是 PHP 的内置函数，用于将图像显示到浏览器或文件。 此函数的主要用途是在浏览器中查看图像，并将任何其他图像类型转换为 WBMP。

**语法：**

```php
*bool* image2wbmp( *resource* $image, *int* $filename, *int* $foreground)
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$filename(可选)：**它指定保存文件的路径。
*   **$forecround(可选)：**它指定图像的前景。

**返回值：**此函数成功时返回 TRUE，错误时返回 FALSE。

下面的示例说明 PHP 中的**image2wbmp()函数**：
**示例 1：**在此示例中，我们将在浏览器中下载图像。

```php
<?php
// Load an wbmp image from local folder
// Image can be converted into wbmp using
// online convertors or imagewbmp()
$im = imagecreatefromwbmp('geeksforgeeks.wbmp');

// Download the image
header('Content-Type: image/vnd.wap.wbmp');
image2wbmp($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will download your image as *download*, 
further you can rename this file to anything like 
*geeksforgeeks.wbmp* and use it.
```

**示例 2：**在此示例中，我们将 PNG 转换为 WBMP。

```php
<?php
// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert the image into WBMP using image2wbmp() function
image2wbmp($im, 'converted.wbmp');
echo 'Image coverted to WBMP successfully.';
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the WBMP version of image 
in the same folder where your PHP script is.
```

**引用：**[https://www.php.net/manual/en/function.image2wbmp.php](https://www.php.net/manual/en/function.image2wbmp.php)