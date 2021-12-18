# PHP|Imagick flipImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-flipimage-function/](https://www.geeksforgeeks.org/php-imagick-flipimage-function/)

**Imagick：：flipImage()**函数是 PHP 中的一个内置函数，用于创建由垂直镜像上的原始图像的镜像反转生成的图像。

**语法：**

```php
*bool* Imagick::flipImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**错误/异常：**它在出错时抛出 ImagickException。

**原始图像：**
![](img/f73b4be7f16e00589c14d824c8603f23.png)

下面的程序演示了 PHP 中的**Imagick：：flipImage()**函数：

**程序：**

```php
<?php 
// require_once('path/vendor/autoload.php'); 

// Create a new Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-14.png');

// Function to flip an Image 
$image->flipImage();

header('Content-type: image/png');

// Display the output image
echo $image;
?>
```

**输出：**
![](img/2954859e93141ca17897b76d0abf53df.png)

**相关文章：**

*   [PHP|Imagick transsposeImage()函数](https://www.geeksforgeeks.org/php-imagick-transposeimage-function/)
*   [PHP|Imagick rotateImage()函数](https://www.geeksforgeeks.org/php-imagick-rotateimage-function/)

**引用：**[http://php.net/manual/en/imagick.flipimage.php](http://php.net/manual/en/imagick.flipimage.php)