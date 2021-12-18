# PHP|Imagick setImageCompressionQuality()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagecompressionquality-function/](https://www.geeksforgeeks.org/php-imagick-setimagecompressionquality-function/)

**Imagick：：setImageCompressionQuality()函数**是 PHP 中的内置函数，用于设置图像压缩质量。

**语法：**

```php
*bool* Imagick::setCompressionQuality( *int* $quality )
```

**参数：**此函数接受单个参数**$quality**，该参数保存表示图像压缩质量的整数值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageCompressionQuality()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression quality
$imagick->setImageCompressionQuality(26);

// Get the Compression quality
$compressionQuality = $imagick->getImageCompressionQuality();
echo $compressionQuality;
?>
```

发帖主题：Re：Колибри0.7.0

```php
26
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression quality
$imagick->setImageCompressionQuality(1);

// Show the output
$imagick->setformat('jpg');
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/58c54733bbaddc09a1c0e5d069ec091b.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagecompressionquality.php](https://www.php.net/manual/en/imagick.setimagecompressionquality.php)