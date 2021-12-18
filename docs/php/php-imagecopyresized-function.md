# PHP|imagecopyresize()函数

> Original: [https://www.geeksforgeeks.org/php-imagecopyresized-function/](https://www.geeksforgeeks.org/php-imagecopyresized-function/)

**imagecopyresize()函数**是 PHP 中的一个内置函数，用于将一个图像的矩形部分复制到另一个图像。 Dst_image 是目标映像，src_image 是源映像标识符。 此函数类似于*imagecopyressamed()*函数，但不进行采样以减小大小。

**语法：**

```php
*bool* imagecopyresized( *resource* $dst_image, 
*resource* $src_image, *int* $dst_x, *int* $dst_y,
 *int* $src_x, *int* $src_y, *int* $dst_w, 
*int* $dst_h, *int* $src_w, *int* $src_h )
```

**参数：**此函数接受上述 10 个参数，如下所述：

*   **$dst_image：**它指定目标图像资源。
*   **$src_image：**它指定源图像资源。
*   **$dst_x：**它指定目标点的 x 坐标。
*   **$dst_y：**它指定目标点的 y 坐标。
*   **$src_x：**它指定源点的 x 坐标。
*   **$src_y：**它指定源点的 y 坐标。
*   **$dst_w：**它指定目标宽度。
*   **$dst_h：**它指定目标高度。
*   **$src_w：**它指定源宽度。
*   **$src_h：**它指定震源高度。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**imagecopyresize()函数**：
**程序 1(将图像大小调整为其宽度和高度的 1.5 倍)：**

```php
<?php
// The percentage to be used
$percent = 1.5;  // make image 1.5 times bigger

// Get image dimensions
list($width, $height) = getimagesize('https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');
$newwidth = $width * $percent;
$newheight = $height * $percent;

// Get the image
$thumb = imagecreatetruecolor($newwidth, $newheight);
$source = imagecreatefromjpeg('https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// Resize the image
imagecopyresized($thumb, $source, 0, 0, 0, 0, $newwidth, $newheight, $width, $height);

// Output the image
header('Content-Type: image/jpeg');
imagejpeg($thumb);
?>
```

**输出：**
![](img/2f27202d8c317f31958701427f3af134.png)

**程序 2(调整固定宽度和高度的图像大小)：**

```php
<?php
// Set a  fixed height and width
$width = 150;
$height = 150;

// Get image dimensions
list($width_orig, $height_orig) = getimagesize('https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

// Resample the image
$image_p = imagecreatetruecolor($width, $height);
$image = imagecreatefromjpeg('https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');
imagecopyresized($image_p, $image, 0, 0, 0, 0, $width, $height, $width_orig, $height_orig);

// Output the image
header('Content-Type: image/jpeg');
imagejpeg($image_p, null, 100);
?>
```

**输出：**
![](img/9162c11a03a42d497b096b8dc8fe8ef8.png)

**引用：**[https://www.php.net/manual/en/function.imagecopyresized.php](https://www.php.net/manual/en/function.imagecopyresized.php)