# PHP|Imagick setCompression()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setcompression-function/](https://www.geeksforgeeks.org/php-imagick-setcompression-function/)

**Imagick：：setCompression()函数**是 PHP 中的一个内置函数，用于设置对象的默认压缩类型。

**语法：**

```php
*bool* Imagick::setCompression( *int* $compression )
```

**参数：**此函数接受单个参数**$COMPRESSION**，该参数保存与[Imagick：：COMPRESSION_*](https://www.php.net/manual/en/imagick.constants.php)常量之一匹配的整数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setCompression()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Get the Compression
$compression = $imagick->getCompression();

echo $compression;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Set the Compression
$imagick->setCompression(5);

// Get the Compression
$compression = $imagick->getCompression();

echo $compression;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setcompression.php](https://www.php.net/manual/en/imagick.setcompression.php)