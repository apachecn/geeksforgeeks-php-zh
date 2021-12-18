# PHP|imagecreatefrom mxpm()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromxpm-function/](https://www.geeksforgeeks.org/php-imagecreatefromxpm-function/)

函数**imagecreatefrom mxpm()**是 PHP 中的一个内置函数，用于从 XPM 文件或 URL 创建新图像。 XPM(X PixMap)是 X Window 系统使用的一种图像文件格式。 这个加载的图像可以在程序中进一步处理。 当您想要在从 XPM 文件加载图像后对其进行编辑时，通常使用此功能。 可以使用各种在线转换器将图像转换为 XPM。

**语法：**

```php
*resource* imagecreatefromxpm( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面的示例说明了 PHP 中的**imagecreatefrom mxpm()函数**：

**示例 1：**转换为 PNG 后查看 XPM。

```php
<?php

// Load an XPM image from local folder
// You can convert any image to XPM using
// Online convertors
$im = imagecreatefromxpm('./geeksforgeeks.xpm');

// Output the image by converting it into PNG
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**示例 2：**编辑 XPM 图像。

```php
<?php

// Load an XPM image from local folder
// You can convert any image to XPM using
// online convertors
$im = imagecreatefromxpm('./geeksforgeeks.xpm');

// Apply Green colorise filter
imagefilter($im, IMG_FILTER_COLORIZE, 0, 200, 0);

// Output the image by converting it into PNG
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/ec706e1c5bcce424dc6f5f930e0583a2.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromxpm.php](https://www.php.net/manual/en/function.imagecreatefromxpm.php)