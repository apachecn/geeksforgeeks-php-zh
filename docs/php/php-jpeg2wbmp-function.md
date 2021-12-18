# PHP|jpeg2wbmp()函数

> Original: [https://www.geeksforgeeks.org/php-jpeg2wbmp-function/](https://www.geeksforgeeks.org/php-jpeg2wbmp-function/)

函数**jpeg2wbmp()**是 PHP 的内置函数，用于将 JPEG 图像文件转换为 WBMP 图像文件。

**语法：**

```
*bool* jpeg2wbmp( *string* $jpegname, 
*int* $wbmpname, *int* $dest_height, 
*int* $dest_width, *int* $threshold )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$jpegname：**它指定 JPEG 文件的路径。
*   **$wbmpname：**它指定目标 WBMP 文件的路径。
*   **$DEST_HEIGHT：**它指定目标图像高度。
*   **$DEST_WIDTH：**它指定目标图像宽度。
*   **$Threshold：**它指定阈值。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**jpeg2wbmp()函数**：
**程序 1：**

```
<?php
// Path to the JPEG image which
// is to be converted
$path = './geeksforgeeks.jpg';

// Get the image sizes which includes
// the height and width
$image = getimagesize($path);
$height = $image[1];
$width = $image[0];

// Convert image the image and save as test.wbmp
jpeg2wbmp($path, './converted.wbmp', $height, $width, 5);
echo 'JPEG converted into WBMP successfully.';
?>
```

发帖主题：Re：Колибри0.7.0

```
This will save the WBMP version of JPEG in the same folder.
```

**程序 2：**

```
<?php
// Path to the JPEG image which
// is to be converted
$path = './geeksforgeeks.jpg';

// Get the image sizes which includes
// the height and width
$image = getimagesize($path);
$height = $image[1];
$width = $image[0];

// Convert image the image and save as test.wbmp
jpeg2wbmp($path, './converted.wbmp', $height, $width, 1);

$im = imagecreatefromwbmp('./converted.wbmp');

header('Content-type: image/png');
imagepng($im);
?>
```

**输出：**
![](img/3052b3b6f9353ca8a037ef905049bd81.png)

**引用：**[https://www.php.net/manual/en/function.jpeg2wbmp.php](https://www.php.net/manual/en/function.jpeg2wbmp.php)