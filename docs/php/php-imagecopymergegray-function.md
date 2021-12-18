# PHP|imagecopymergeGrey()函数

> Original: [https://www.geeksforgeeks.org/php-imagecopymergegray-function/](https://www.geeksforgeeks.org/php-imagecopymergegray-function/)

**imagecopymergeGrey()**函数是 PHP 中的一个内置函数，用于复制和合并具有灰度的图像部分。 此函数用于将源映像的一部分复制到目标映像。 此函数成功时返回 TRUE，失败时返回 FALSE。

**语法：**

```php
bool imagecopymergegray ( $dst_image, $src_image, $dst_x, $dst_y, $src_x, $src_y, 
$src_w, $src_h, $pct )
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
*   **$pct：**此参数用于根据$pct 更改灰度。 $%的范围是 0 到 100，其中 0 表示完全灰度，100 表示不变。 如果$pct=0，则不执行任何操作，当$pct=100 时，此函数的行为类似于苍白图像的 imagecopy()函数，只是忽略 Alpha 分量。 它实现了真彩色图像的 Alpha 透明度。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**imagecopymergeGrey()**函数：

**程序 1：**

```php
<?php

// Create image instances
$dest = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

$src = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/slider.gif');

// Copy and merge the image
imagecopymergegray($dest, $src, 10, 10, 0, 0, 700, 200, 75);

// Output and free from memory
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![image](img/6469e5672024e507f857833c21c1e10f.png)

**程序 2：**

```php
<?php
// Create image instances
$dest = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');
$src = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/temp1.png');

// Copy and merge
imagecopymergegray($dest, $src, 10, 10, 0, 0, 700, 200, 75);

// Output and free from memory
header('Content-Type: image/png');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

**输出：**
![image](img/d14033e4cbcbcea0e9913abd8e28cb05.png)

**相关文章：**

*   [PHP|imagecopy()函数](https://www.geeksforgeeks.org/php-imagecopy-function/)
*   [PHP|imagecopymerge()函数](https://www.geeksforgeeks.org/php-imagecopymerge-function/)

**引用：**[http://php.net/manual/en/function.imagecopymergegray.php](http://php.net/manual/en/function.imagecopymergegray.php)