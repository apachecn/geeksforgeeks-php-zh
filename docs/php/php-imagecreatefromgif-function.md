# PHP|imagecreatefrom mgif()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromgif-function/](https://www.geeksforgeeks.org/php-imagecreatefromgif-function/)

**imagecreatefrom mgif()函数**是 PHP 中的一个内置函数，用于从 GIF 文件或 URL 的给定部分创建新图像。 此外，这个图像可以在程序中处理。 此函数仅加载动画的第一帧。

**语法：**

```php
*resource* imagecreatefromgif( *string* $filename )
```

**参数：**此函数接受保存图像的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面的示例说明了 PHP 中的**imagecreatefrom mgif()函数**：

**示例 1：**在浏览器中加载第一帧。

```php
<?php

// Create an image from gif
$im = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// View the image
header("Content-Type: image/gif");
imagegif($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**示例 2：**将第一帧保存为本地文件夹中的 JPG

```php
<?php

// Create an image from gif
$im = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// Save the image as jpeg
imagejpeg($im, 'firstframe.jpg');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the first frame as firstframe.jpg in the same folder.
```

**注意：**图像资源指针中只返回第一帧。

**引用：**[https://www.php.net/manual/en/function.imagecreatefromgif.php](https://www.php.net/manual/en/function.imagecreatefromgif.php)