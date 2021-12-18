# PHP|Imagick getImageCompression()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagecompression-function/](https://www.geeksforgeeks.org/php-imagick-getimagecompression-function/)

**Imagick：：getImageCompression()函数**是 PHP 中的一个内置函数，用于获取当前图像的压缩类型。

**语法：**

```
*int* Imagick::getImageCompression( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，该整数值对应于一个压缩常数。

下面给出了**压缩常量**的列表：

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

以下程序说明 PHP：
**程序 1：**中的**Imagick：：getImageCompression()函数**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Compression
$compression = $imagick->getImageCompression();
echo $compression;
?>
```

发帖主题：Re：Колибри0.7.0

```
13
```

**程序 2：**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression to COMPRESSION_DXT1
$imagick->setImageCompression(imagick::COMPRESSION_DXT1);

// Get the Compression
$compression = $imagick->getImageCompression();

echo $compression;
?>
```

发帖主题：Re：Колибри0.7.0

```
3
```

**引用：**[https://www.php.net/manual/en/imagick.getimagecompression.php](https://www.php.net/manual/en/imagick.getimagecompression.php)