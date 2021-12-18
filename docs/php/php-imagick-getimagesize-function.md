# PHP|Imagick getImageSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagesize-function/](https://www.geeksforgeeks.org/php-imagick-getimagesize-function/)

**Imagick：：getImageSize()函数**是 PHP 中的一个内置函数，用于获取以字节为单位的图像长度。

**语法：**

```
*int* Imagick::getImageSize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含当前图像大小的整数值。

下面的程序说明了 PHP 中的**Imagick：：getImageSize()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Image Size
$size = $imagick->getImageSize();
echo 'Image size is '. $size . ' bytes.';
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the Image Size
$size = $imagick->getImageSize();
echo 'Image size is '. $size . ' bytes.';
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagesize.php](https://www.php.net/manual/en/imagick.getimagesize.php)