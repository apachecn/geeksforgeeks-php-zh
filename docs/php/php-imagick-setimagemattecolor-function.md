# PHP|Imagick setImageMatteColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagemattecolor-function/](https://www.geeksforgeeks.org/php-imagick-setimagemattecolor-function/)

**Imagick：：setImageMatteColor()函数**是 PHP 中的一个内置函数，用于设置图像遮罩颜色。

**语法：**

```php
*bool* Imagick::setImageMatteColor( *mixed* $matte )
```

**参数：**此函数接受保存图像遮罩颜色的单个参数**$matte**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageMatteColor()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Matte Color Pixel
$imagick->setImageMatteColor('skyblue');

// Get the Matte Color Pixel
$matteColorPixel = $imagick->getImageMatteColor();

// Convert ImagickPixel into Color
$matteColor = $matteColorPixel->getColorAsString();
echo $matteColor;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Matte Color Pixel
$imagick->setImageMatteColor('turquoise');

// Get the Matte Color Pixel
$matteColorPixel = $imagick->getImageMatteColor();

// Convert ImagickPixel into Color
$matteColor = $matteColorPixel->getColorAsString();
echo $matteColor;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimagemattecolor.php](https://www.php.net/manual/en/imagick.setimagemattecolor.php)