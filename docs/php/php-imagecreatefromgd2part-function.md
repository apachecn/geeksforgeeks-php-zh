# PHP|imagecreatefrom mgd2part()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromgd2part-function/](https://www.geeksforgeeks.org/php-imagecreatefromgd2part-function/)

函数**imagecreatefrom mgd2part()**是 PHP 中的一个内置函数，用于从 GD2 文件或 URL 的给定部分创建新图像。 此外，这个图像可以在程序中处理。 通常，浏览器不支持 GD2 扩展，因此可以使用它将其转换为 PNG 并在浏览器中查看。

**语法：**

```php
*resource* imagecreatefromgdpart( *string* $filename,
         *int* $srcX, *int* $srcY, *int* $width, *int* $height )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$filename：**它指定 GD2 映像。
*   **$srcX：**它指定源点的 x 坐标。
*   **$srcY：**它指定源点的 y 坐标。
*   **$width：**它指定图像的宽度。
*   **$Height：**它指定图像的高度。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序演示了 PHP 中的**imagecreatefrom mgd2part()函数**：

**程序 1(在浏览器中查看 GD2 文件)：**

```php
<?php

// Load the GD2 image from local folder GD2 images
// can be created with imagegd2() function
$im = imagecreatefromgd2part('./geeksforgeeks.gd2',
                   300, 0, 300, 300);

// Convert to PNG and output to the browser
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/0f557a6648ab72207acd797904c7cb8b.png)

**程序 2(将 gd2 转换为 jpeg)：**

```php
<?php

// Load the GD2 image from local folder GD2 images
// can be created with imagegd2() function
$im = imagecreatefromgd2part('./geeksforgeeks.gd2',
                 30, 0, 100, 250);

// Convert to JPEG and save to local folder
imagejpeg($im, 'newgeeksforgeeks.jpeg');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
It will load the part of image and convert it
into JPEG and saves it into same folder.
```

**引用：**[https://www.php.net/manual/en/function.imagecreatefromgd2part.php](https://www.php.net/manual/en/function.imagecreatefromgd2part.php)