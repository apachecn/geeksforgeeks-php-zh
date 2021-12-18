# PHP|Imagick setImageFormat()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageformat-function/](https://www.geeksforgeeks.org/php-imagick-setimageformat-function/)

**Imagick：：setImageFormat()函数**是 PHP 中的内置函数，用于设置序列中特定图像的格式。

**语法：**

```
*bool* Imagick::setImageFormat( *string* $format )
```

**参数：**此函数接受单个参数**$format**，该参数保存图像格式(如 PNG、SVG 等)的字符串值。格式支持完全取决于 Imagick 的安装。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setImageFormat()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Format
$imagick->setImageFormat('png');

// Get the Filename
$format = $imagick->getImageFormat();
echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Format
$imagick->setImageFormat('jpeg');

// Get the Format
$format = $imagick->getImageFormat();
echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimageformat.php](https://www.php.net/manual/en/imagick.setimageformat.php)