# PHP|Imagick choImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-chopimage-function/](https://www.geeksforgeeks.org/php-imagick-chopimage-function/)

**Imagick：：choImage()**函数是 PHP 中的一个内置函数，用于删除图像区域并对其进行修剪。 此函数接受图像的尺寸，并对要裁剪图像的区域和尺寸进行裁切。

**语法：**

```php
*bool* Imagick::chopImage( $width, $height, $x, $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width：**此参数存储斩波区域的宽度。
*   **$Height：**此参数存储切割区域的高度。
*   **$x：**此参数存储斩波区域的 x 原点。
*   **$y：**此参数存储切割区域的 y 原点。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f73b4be7f16e00589c14d824c8603f23.png)

下面的程序演示了 PHP 中的**Imagick：：choImage()**函数：

**程序：**

```php
<?php 
// require_once('path/vendor/autoload.php'); 

// Create a new Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-14.png');

// chopImage function
$image->chopImage(40, 35, 1, 2);

header('Content-type: image/png');

// Display the output image
echo $image;
?>
```

**输出：**
![](img/ced86e78095607b63d11651f13a2feaa.png)

**相关文章：**

*   [PHP|Imagick autoLevelImage()函数](https://www.geeksforgeeks.org/php-imagick-autolevelimage-function/)
*   [PHP|Imagick borderImage()函数](https://www.geeksforgeeks.org/php-imagick-borderimage-function/)

**引用：**[http://php.net/manual/en/imagick.chopimage.php](//php.net/manual/en/imagick.chopimage.php)