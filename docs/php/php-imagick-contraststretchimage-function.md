# PHP|Imagick 对比度 StretchImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-contraststretchimage-function/](https://www.geeksforgeeks.org/php-imagick-contraststretchimage-function/)

**Imagick：：ConstrastStretchImage()函数**是 PHP 中的一个内置函数，用于增强图像的对比度。 此功能通过调整像素颜色以覆盖整个可用颜色范围来增强彩色图像的对比度。

**语法：**

```php
*bool* Imagick::contrastStretchImage( *float* $black_point,
         *float* $white_point, *int* $channel = Imagick::CHANNEL_DEFAULT)
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$BLACK_POINT：**此参数保存黑点。
*   **$White_point：**此参数保存白点。
*   **$channel：**此参数保存 Imagick 通道常量，这些常量提供对通道模式有效的任何通道常量。 可以使用按位运算符组合多个通道。 通道常量的默认值为 CHANNEL_DEFAULT。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**Imagick：：ConstrastStretchImage()函数**：

**程序 1：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the contrastStretchImage() function
$imagick->contrastStretchImage(10, 20);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/541a5e3daf8f2b114cc30b7c77faf7d8.png)

**程序 2：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the contrastStretchImage() function
$imagick->contrastStretchImage(100, 50);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/33269cd230a8fee3e4ee55cf14ab41ad.png)

**程序 3：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the contrastStretchImage() function
$imagick->contrastStretchImage(5000, 100);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/6756147a703acb47dcfbc301b0c722d3.png)

**引用：**[https://www.php.net/manual/en/imagick.contraststretchimage.php](https://www.php.net/manual/en/imagick.contraststretchimage.php)