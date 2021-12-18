# PHP|Imagick getImageRegion()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageregion-function/](https://www.geeksforgeeks.org/php-imagick-getimageregion-function/)

**Imagick：：getImageRegion()函数**是 PHP 中的一个内置函数，用于提取图像的一个区域。

**语法：**

```php
*Imagick* Imagick::getImageRegion( *int* $width, *int* $height, *int* $x, *int* $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width：**它指定提取区域的宽度。
*   **$Height：**它指定提取区域的高度。
*   **$x：**指定提取区域左上角的 x 坐标。
*   **$y：**它指定提取区域左上角的 y 坐标。

**返回值：**此函数将新区域作为新的条形返回。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：getImageRegion()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Image Region
$region = $imagick->getImageRegion(300, 160, 0, 0);

// Add border
$region->borderImage('green', 1, 1);

// Display the image
header("Content-Type: image/png");
echo $region->getImageBlob();
?>
```

**输出：**
![](img/b11bd2db1cbbb8bcfaf672539673cde2.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Image Region
$region = $imagick->getImageRegion(300, 160, 100, 0);

// Add border
$region->borderImage('green', 1, 1);

// Display the image
header("Content-Type: image/png");
echo $region->getImageBlob();
?>
```

**输出：**
![](img/f20f4937c60a7a52d3d34c5db7058c98.png)

**引用：**[https://www.php.net/manual/en/imagick.getimageregion.php](https://www.php.net/manual/en/imagick.getimageregion.php)