# PHP|imagecreatefrom mxbm()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromxbm-function/](https://www.geeksforgeeks.org/php-imagecreatefromxbm-function/)

函数**imagecreatefrom mxbm()**是 PHP 中的一个内置函数，用于从 XBM 文件或 URL 创建新图像。 XBM 文件扩展名是用于图形 UI 系统的 X 位图图形文件。 这个加载的图像可以在程序中进一步处理。 当您想要在从 XBM 文件加载图像后对其进行编辑时，通常使用此函数。 可以使用*imagexbm()*函数将图像转换为 XBM。

**语法：**

```
*resource* imagecreatefromxbm( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序说明了 PHP 中的**imagecreatefrom mxbm()函数**：
**程序 1：**

```
<?php
// Load an XBM image from local folder
// You can convert any image to XBM using
// imagexbm() function or online convertors
$im = imagecreatefromxbm('./geeksforgeeks.xbm');

// View the loaded image in browser
imagexbm($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```
This will load the content into browser in the form of unsupported text as browsers don't support XBM.
```

**程序 2：**

```
<?php
// Load an XBM image from local folder
// You can convert any image to XBM using
// imagexbm() function or online convertors
$im = imagecreatefromxbm('./geeksforgeeks.xbm');

// Output the image by converting it into PNG
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromxbm.php](https://www.php.net/manual/en/function.imagecreatefromxbm.php)