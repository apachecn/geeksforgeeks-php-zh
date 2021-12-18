# PHP|png2wbmp()函数

> Original: [https://www.geeksforgeeks.org/php-png2wbmp-function/](https://www.geeksforgeeks.org/php-png2wbmp-function/)

函数**png2wbmp()**是 PHP 的内置函数，用于将 PNG 图像文件转换为 WBMP 图像文件。

**语法：**

```php
*bool* png2wbmp( *string* $pngname, 
*int* $wbmpname, *int* $dest_height, 
*int* $dest_width, *int* $threshold )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$pngname：**它指定 PNG 文件的路径。
*   **$wbmpname：**它指定目标 WBMP 文件的路径。
*   **$DEST_HEIGHT：**它指定目标图像高度。
*   **$DEST_WIDTH：**它指定目标图像宽度。
*   **$Threshold：**它指定阈值。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**png2wbmp()函数**：
**程序 1：**

```php
<?php
// Path to the PNG image which
// is to be converted
$path = './geeksforgeeks.png';

// Get the image sizes which includes
// the height and width
$image = getimagesize($path);
$height = $image[1];
$width = $image[0];

// Convert image the image and save as test.wbmp
png2wbmp($path, './converted.wbmp', $height, $width, 5);
echo 'PNG converted into WBMP successfully.';
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the WBMP version of PNG in the same folder.
```

**程序 2：**

```php
<?php
// Path to the PNG image which
// is to be converted
$path = './geeksforgeeks.jpg';

// Get the image sizes which includes
// the height and width
$image = getimagesize($path);
$height = $image[1];
$width = $image[0];

// Convert image the image and save as test.wbmp
png2wbmp($path, './converted.wbmp', $height, $width, 3);

$im = imagecreatefromwbmp('./converted.wbmp');

header('Content-type: image/png');
imagepng($im);
?>
```

**输出：**
![](img/82c2477bfc831c58f9a66d8af3e4d95e.png)

**引用：**[https://www.php.net/manual/en/function.png2wbmp.php](https://www.php.net/manual/en/function.png2wbmp.php)