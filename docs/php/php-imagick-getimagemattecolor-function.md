# PHP|Imagick getImageMatteColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagemattecolor-function/](https://www.geeksforgeeks.org/php-imagick-getimagemattecolor-function/)

**Imagick：：getImageMatteColor()**函数是 PHP 中的一个内置函数，用于获取图像遮罩颜色。

**语法：**

```
*ImagickPixel* Imagick::getImageMatteColor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像遮罩颜色的 ImagickPixel 对象。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageMatteColor()**函数：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Matte Color Pixel
$matteColorPixel = $imagick->getImageMatteColor();

// Convert ImagickPixel into Color
$matteColor = $matteColorPixel->getColorAsString();
echo $matteColor;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Matte Color Pixel
$imagick->setImageMatteColor('purple');

// Get the Matte Color Pixel
$matteColorPixel = $imagick->getImageMatteColor();

// Convert ImagickPixel into Color
$matteColor = $matteColorPixel->getColorAsString();
echo $matteColor;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagemattecolor.php](https://www.php.net/manual/en/imagick.getimagemattecolor.php)