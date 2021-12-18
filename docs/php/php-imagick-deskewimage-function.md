# PHP|Imagick deskewImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-deskewimage-function/](https://www.geeksforgeeks.org/php-imagick-deskewimage-function/)

Imagick：：deskewImage()函数是 PHP 中的一个内置函数，用于对图像进行去倾斜或从图像中移除倾斜。 如果 Imagick 针对 Imagick 版本 6.4.5 或更高版本进行编译，则此功能可用。 当相机未对齐或纸张未放置在平面上时，会出现**倾斜**方法。

**语法：**

```
*bool* Imagick::deskewImage( $threshold )
```

**参数：**此函数接受单个参数$Threshold，该参数保存去歪斜阈值的值。

**返回值：**此函数返回布尔值。

下面的程序演示了 PHP 中的 Imagick：：deskewImage()函数：

**程序：**

```
<?php

// Create new Imagick object
$imagick = new \Imagick(
"https://contribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png");

// Clone the Imagick object
$deskew = clone $imagick;

// Initialize the threshold value
$threshold = 0.5;

// Use deskewImage() function to deskew the image
$deskew->deskewImage($threshold);

header("Content-Type: image/jpg");

// Display the deskew image
echo $deskew->getImageBlob();

?>
```

**输出：**
![deskew image](img/e5e11429c8889b9427ac9344443a5d4f.png)

**引用：**[https://www.php.net/manual/en/imagick.deskewimage.php](https://www.php.net/manual/en/imagick.deskewimage.php)