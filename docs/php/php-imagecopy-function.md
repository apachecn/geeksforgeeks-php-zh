# PHP|imagecopy()函数

> Original: [https://www.geeksforgeeks.org/php-imagecopy-function/](https://www.geeksforgeeks.org/php-imagecopy-function/)

**imagecopy()**函数是 PHP 中的一个内置函数，用于复制图像或图像的一部分。 此函数成功时返回 TRUE，失败时返回 FALSE。

**语法：**

```php
*bool* imagecopy ( $dst_image, $src_image, $dst_x, $dst_y, $src_x, 
$src_y, $src_w, $src_h )
```

**参数：**此函数接受上述 8 个参数，如下所述：

*   **$dst_image：**该参数用于设置目标图片链接资源。
*   **$src_image：**该参数用于设置源图片链接资源。
*   **$dst_x：**此参数用于设置目标点的 x 坐标。
*   **$dst_y：**此参数用于设置目标点的 y 坐标。
*   **$src_x：**该参数用于设置震源点的 x 坐标。
*   **$src_y：**该参数用于设置震源点的 x 坐标。
*   **$src_w：**此参数用于设置源宽度。
*   **$src_h：**该参数用于设置震源高度。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的**imagecopy()**函数。

**程序 1：**

```php
<?php

// Create image instances
$src = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');
$dest = imagecreatetruecolor(400, 200);

// Image copy from source to destination
imagecopy($dest, $src, 0, 0, 0, 0, 500, 300);

// Output and free from memory
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![part of image](img/6a45dd8304b82b11f901b3e8540767f1.png)

**程序 2：**

```php
<?php
// Create image instances
$src = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');
$dest = imagecreatetruecolor(665, 180);

// Image copy from source to destination
imagecopy($dest, $src, 0, 0, 0, 0, 665, 180);

// Output and free from memory
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![full image](img/2404db22edc3d4e67cac29e6b346ffd9.png)

**相关文章：**

*   [PHP|imagecolorallocatealpha()函数](https://www.geeksforgeeks.org/php-imagecolorallocatealpha-function/)
*   [PHP|imagepolygon()函数](https://www.geeksforgeeks.org/php-imagepolygon-function/)

**引用：**[http://php.net/manual/en/function.imagecopy.php](http://php.net/manual/en/function.imagecopy.php)