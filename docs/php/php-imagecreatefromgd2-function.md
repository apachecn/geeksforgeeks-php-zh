# PHP|imagecreatefrom mgd2()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromgd2-function/](https://www.geeksforgeeks.org/php-imagecreatefromgd2-function/)

**imagecreatefrom mgd2()函数**是 PHP 中的一个内置函数，用于从文件或 URL 创建新图像。 此外，这个图像可以在程序中处理。 通常，浏览器不支持 GD2 扩展，因此可以使用它将其转换为 PNG 并在浏览器中查看。

**语法：**

```
resource imagecreatefromgd2( string $filename )
```

**参数：**此函数接受单个参数**$fileName**，该参数保存文件的名称或 URL。
**返回值：**此函数成功时返回图片资源标识符，出错时返回 False。

下面给出的程序说明了 PHP 中的**imagecreatefrom mgd2()函数**：
**程序 1(在浏览器中查看 GD2 文件)：**

## PHP

```
<?php
// Load the GD2 image from local folder
// GD2 images can be created with imagegd2() function
$im = imagecreatefromgd2('geeksforgeeks.gd2');

// Convert to PNG and output to the browser
header('Content-type: image/png');  
imagepng($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2(将 gd2 转换为 jpeg)：**

## PHP

```
<?php
// Load the GD2 image
$im = imagecreatefromgd2('geeksforgeeks.gd2');

// Convert it to a JPEG file, press Ctrl + S to save the new jpeg image
header('Content-type: image/jpeg');  
imagejpeg($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/b45812a96b6414e34678dd59ee7e3040.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromgd2.php](https://www.php.net/manual/en/function.imagecreatefromgd2.php)