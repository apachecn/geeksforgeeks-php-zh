# PHP|Imagick getImageWidth()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagewidth-function/](https://www.geeksforgeeks.org/php-imagick-getimagewidth-function/)

**Imagick：：getImageWidth()**函数是 PHP 中的一个内置函数，用于获取图像的宽度。

**语法：**

```php
*int* Imagick::getImageWidth( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回图像宽度(以像素为单位)。

**原始图像**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

下面的程序说明了 PHP：
**程序：**中的**Imagick：：getImageWidth()**函数

```php
<?php 
// require_once('path/vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Function to get the width of image
$width = $image->getImageWidth();

// Display the image width in pixel.
print_r($width);
?>
```

发帖主题：Re：Колибри0.7.0

```php
667
```

**相关文章：**

*   [PHP|Imagick autoLevelImage()函数](https://www.geeksforgeeks.org/php-imagick-autolevelimage-function/)
*   [PHP|Imagick VignetteImage()函数](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)

**引用：**[http://php.net/manual/en/imagick.getimagewidth.php](http://php.net/manual/en/imagick.getimagewidth.php)