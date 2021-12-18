# PHP|Imagick setCompressionQuality()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setcompressionquality-function/](https://www.geeksforgeeks.org/php-imagick-setcompressionquality-function/)

**Imagick：：setCompressionQuality()函数**是 PHP 中的一个内置函数，用于设置对象的默认压缩质量。

**语法：**

```
*bool* Imagick::setCompressionQuality( *int* $quality )
```

**参数：**此函数接受单个参数**$quality**，该参数保存表示质量的整数值。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setCompressionQuality()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression quality
$imagick->setCompressionQuality(25);

// Get the Compression quality
$compressionQuality = $imagick->getCompressionQuality();

echo $compressionQuality;
?>
```

发帖主题：Re：Колибри0.7.0

```
25
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the Compression quality to 1
$imagick->setCompressionQuality(1);

// Write the caption in a image
$imagick->newPseudoImage(800, 320, "caption:GeekforGeeks");
$imagick->floodfillPaintImage("orange", 1, "white", 1, 1, false);

// Show the output
$imagick->setformat('jpg');
header("Content-Type: image/jpg");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/26d7b38e7f537610256956f4ce7072ee.png)

**引用：**[https://www.php.net/manual/en/imagick.setcompressionquality.php](https://www.php.net/manual/en/imagick.setcompressionquality.php)