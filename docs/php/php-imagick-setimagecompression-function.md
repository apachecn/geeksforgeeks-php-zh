# PHP|Imagick setImageCompression()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagecompression-function/](https://www.geeksforgeeks.org/php-imagick-setimagecompression-function/)

**Imagick：：setImageCompression()函数**是 PHP 中的内置函数，用于设置图像压缩类型。

**语法：**

```
*bool* Imagick::setImageCompression( *int* $compression )
```

**参数：**此函数接受单个参数**$COMPRESSION**，该参数保存与[Imagick：：COMPRESSION_*](https://www.php.net/manual/en/imagick.constants.php)常量之一匹配的整数。 此外，您可以像
*$Imagick->setImageCompression(imagick：：COMPRESSION_DXT1)；*那样直接传递常量。

压缩常量列表如下：

*   Imagick：：COMPRESSION_UNDEFINED(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==引用=外部链接==
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：COMPRESSION_GROUP4(7)
*   Imagick：：COMPRESSION_JPEG(8)
*   ==引用=外部链接==
*   图片：：同情 _LOSSLESSJPEG(10)
*   Imagick：：Compensation_LZW(11)
*   图片：：慈悲 _RLE(12)
*   图片：：同情心 _zip(13)
*   Imagick：：Underming_DXT1(3)
*   Imagick：：COMPLETION_DXT3(4)
*   ==同步，由 Elderman 更正==@ELDER_MAN

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageCompression()函数**：

**程序 1：**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression to COMPRESSION_RLE
$imagick->setImageCompression(imagick::COMPRESSION_RLE);

// Get the Compression
$compression = $imagick->getImageCompression();
echo $compression;
?>
```

发帖主题：Re：Колибри0.7.0

```
12
```

**程序 2：**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression to COMPRESSION_JPEG
$imagick->setImageCompression(imagick::COMPRESSION_JPEG);

// Set the Compression quality
// This is where that compression method imagick::COMPRESSION_JPEG is
// used in the program.
$imagick->setImageCompressionQuality(5);

// Show the output
$imagick->setformat('jpg');
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/fa972a44b308d03f317837ed9726e945.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagecompression.php](https://www.php.net/manual/en/imagick.setimagecompression.php)