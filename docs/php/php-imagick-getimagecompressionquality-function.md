# PHP|Imagick getImageCompressionQuality()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagecompressionquality-function/](https://www.geeksforgeeks.org/php-imagick-getimagecompressionquality-function/)

**Imagick：：getImageCompressionQuality()函数**是 PHP 中的一个内置函数，用于诱导当前图像的压缩质量。

**语法：**

```
*int* Imagick::getImageCompressionQuality( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含当前图像压缩质量的整数值。

下面的程序演示了 PHP 中的**Imagick：：getImageCompressionQuality()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Compression quality
$compressionQuality = $imagick->getImageCompressionQuality();

echo $compressionQuality;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression quality
$imagick->setImageCompressionQuality(65);

// Get the Compression quality
$compressionQuality = $imagick->getImageCompressionQuality();

echo $compressionQuality;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagecompressionquality.php](https://www.php.net/manual/en/imagick.getimagecompressionquality.php)