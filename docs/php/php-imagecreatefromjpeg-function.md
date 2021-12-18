# PHP|imagecreatefrom mjpeg()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromjpeg-function/](https://www.geeksforgeeks.org/php-imagecreatefromjpeg-function/)

函数**imagecreatefrom mjpeg()**是 PHP 中的一个内置函数，用于从 JPEG 文件或 URL 创建新图像。 这个图像可以在程序中进一步处理。

**语法：**

```php
resource imagecreatefromjpeg( string $filename )
```

**参数：**此函数接受单个参数**$filename**，该参数保存图像的名称
**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面的示例说明了 PHP 中的**imagecreatefrom mjpeg()函数**：

**示例 1：**

## PHP

```php
<?php

// Load an image from jpeg URL
$im = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// View the loaded image in browser
header('Content-type: image/jpg');  
imagejpeg($im);
imagedestroy($im);
?>
```

**输出：**
![](img/7e9f49eb7ab8ebe395bc569571a3eafd.png)

**示例 2：**

```php
<?php

// Load an image from jpeg URL
$im = imagecreatefromjpeg(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// Flip the image
imageflip($im, 1);

// View the loaded image in browser
header('Content-type: image/jpg');  
imagejpeg($im);
imagedestroy($im);
?>
```

**输出：**
![](img/70191b4ce9ec9d0680a8c00869db227e.png)
**参考：**[https://www.php.net/manual/en/function.imagecreatefromjpeg.php](https://www.php.net/manual/en/function.imagecreatefromjpeg.php)