# PHP|Imagick VignetteImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)

**Imagick：：VignetteImage()**函数是 PHP 中的一个内置函数，用于向图像添加老式滤镜。 此函数用于说明或描绘淡入背景而没有明确边界的图像。

**语法：**

```php
bool Imagick::vignetteImage( $blackPoint, $whitePoint, $x, $y )

```

**参数：**此函数接受上述四个参数，如下所述：

*   **$BLACKPOINT：**该参数用于存储黑点的值。
*   **$WhitePoint：**此参数用于存储白点的值。
*   **$x：**此参数存储椭圆的 X 偏移量的值。
*   **$y：**此参数存储椭圆的 Y 偏移值。

**返回值：**成功时此函数返回 True。
**原始图像：**
![](img/f73b4be7f16e00589c14d824c8603f23.png)

下面的程序演示了 PHP 中的**Imagick：：VignetteImage()**函数：

**程序：**

```php
<?php 
// require_once('path/vendor/autoload.php'); 

// Create an Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-12.png');

// vignetteImage Function 
$imagick->vignetteImage(35.6, 11.8, 40, 15);

// Image Header
header("Content-Type: image/jpg");

// Display image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/ab049fa38f1ebf24ba5b8919b31837b8.png)

**相关文章：**

*   [PHP|Imagick transsposeImage()函数](https://www.geeksforgeeks.org/php-imagick-transposeimage-function/)
*   [PHP|Imagick rotateImage()函数](https://www.geeksforgeeks.org/php-imagick-rotateimage-function/)

**引用：**[http://php.net/manual/en/imagick.vignetteimage.php](http://php.net/manual/en/imagick.vignetteimage.php)