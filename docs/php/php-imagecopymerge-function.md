# PHP|imagecopymerge()函数

> Original: [https://www.geeksforgeeks.org/php-imagecopymerge-function/](https://www.geeksforgeeks.org/php-imagecopymerge-function/)

**imagecopymerge()**函数是 PHP 中的一个内置函数，用于复制图像并将其合并为单个图像。 此函数成功时返回 True，失败时返回 False。

**语法：**

```php
*bool* imagecopymerge ( $dst_image, $src_image, $dst_x, $dst_y, 
$src_x, $src_y, $src_w, $src_h, $pct )
```

**参数：**此函数接受上述 9 个参数，如下所述：

*   **$dst_image：**该参数用于设置目标图片链接资源。
*   **$src_image：**该参数用于设置源图片链接资源。
*   **$dst_x：**此参数用于设置目标点的 x 坐标。
*   **$dst_y：**此参数用于设置目标点的 y 坐标。
*   **$src_x：**该参数用于设置震源点的 x 坐标。
*   **$src_y：**该参数用于设置震源点的 x 坐标。
*   **$src_w：**此参数用于设置源宽度。
*   **$src_h：**该参数用于设置震源高度。
*   **$pct：**这两个图像将在*$pct*变量的帮助下合并。 百分比的范围是 0 到 100。 如果$pct=0，则不执行任何操作，当$pct=100 时，此函数的行为类似于苍白图像的 imagecopy()函数，只是忽略 Alpha 分量。 它实现了真彩色图像的 Alpha 透明度。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的**imagecopymerge()**函数：

**程序 1：**
**输入源图像：**
![source image](img/ac3a1f3632dfb8090a5e3d0b63102129.png)
**输入目标图像：**
![destination image](img/b7905e631526ae6974f1fc5a421df498.png)

```php
<?php
// Create image instances
$dest = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');
$src = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/slider.gif');

// Copy and merge
imagecopymerge($dest, $src, 10, 10, 0, 0, 500, 200, 75);

// Output and free from memory
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![copy merge image](img/b23c978cc2d0343c81d23f4b9b051554.png)

**程序 2：**
**输入源图像：**
![source image](img/ff84c5f254645034806d5748a28af55a.png)
**输入目标图像：**
![destination image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

```php
<?php
// Create image instances
$dest = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');
$src = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/col1.png');

// Copy and merge
imagecopymerge($dest, $src, 10, 10, 0, 0, 500, 200, 75);

// Output and free from memory
header('Content-Type: image/png');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![copy merge image](img/d3a6fccba874bbeabd5f5a5d81789aba.png)

**相关文章：**

*   [PHP|imagecolorclosestapha()函数](https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/)
*   [PHP|imagecolorallocatealpha()函数](https://www.geeksforgeeks.org/php-imagecolorallocatealpha-function/)
*   [PHP|图像颜色分配()函数](https://www.geeksforgeeks.org/php-imagecolorallocate-function/)

**引用：**[http://php.net/manual/en/function.imagecopymerge.php](http://php.net/manual/en/function.imagecopymerge.php)