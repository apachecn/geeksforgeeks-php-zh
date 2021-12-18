# PHP|Imagick MagnifyImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-magnifyimage-function/](https://www.geeksforgeeks.org/php-imagick-magnifyimage-function/)

**Imagick：：MagnifyImage()**函数是 PHP 中的一个内置函数，用于将图像按比例缩放到 2 倍。 此函数用于将图像缩放为其原始大小的两倍。

**语法：**

```php
bool Imagick::magnifyImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f73b4be7f16e00589c14d824c8603f23.png)

下面的程序演示了 PHP 中的**Imagick：：MagnifyImage()**函数：

**程序：**

```php
<?php
/*require_once('path/vendor/autoload.php');*/

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-12.png');

// Magnify Image

$image->magnifyImage();

// Image Header

header("Content-Type: image/jpg");

// Display the image
echo $image;
?>
```

**输出：**
![](img/040a9782347712cff976a5f556a3c80c.png)

**相关文章：**

*   [PHP|Imagick 注解图像()函数](https://www.geeksforgeeks.org/php-imagick-annotateimage-function/)
*   [PHP|Imagick transsposeImage()函数](https://www.geeksforgeeks.org/php-imagick-transposeimage-function/)

**引用：**[http://php.net/manual/en/imagick.magnifyimage.php](http://php.net/manual/en/imagick.magnifyimage.php)