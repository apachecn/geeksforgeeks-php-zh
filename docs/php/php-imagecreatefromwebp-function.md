# PHP|imagecreatefrom mwebp()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromwebp-function/](https://www.geeksforgeeks.org/php-imagecreatefromwebp-function/)

函数**imagecreatefrom mwebp()**是 PHP 中的一个内置函数，用于从 WebP 文件或 URL 创建新图像。 WebP 是一种同时采用有损和无损压缩的图像格式。 这个图像可以在程序中进一步处理。 当您想要在从 WebP 文件加载图像后对其进行编辑时，通常使用此功能。 可以使用*imagewebp()*函数将图像转换为 WebP。

**语法：**

```
*resource* imagecreatefromwebp( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序演示了 PHP 中的**imagecreatefrom mwebp()函数**：

**程序 1：**

```
<?php
// Load an WEBP image from local folder
// You can convert any image to WEBP using
// imagewebp() function or online convertors
$im = imagecreatefromwebp('./geeksforgeeks.webp');

// View the loaded image in browser
imagewebp($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

> 这将以不支持的文本形式将内容加载到浏览器中，因为浏览器不支持 WebP。

**程序 2：**

```
<?php
// Load an WEBP image from local folder
// You can convert any image to WEBP using
// imagewebp() function or online convertors
$im = imagecreatefromwebp('./geeksforgeeks.webp');

// Output the image by converting it into PNG
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromwebp.php](https://www.php.net/manual/en/function.imagecreatefromwebp.php)