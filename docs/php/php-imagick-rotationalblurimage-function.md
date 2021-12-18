# PHP|Imagick rotationalBlurImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-rotationalblurimage-function/](https://www.geeksforgeeks.org/php-imagick-rotationalblurimage-function/)

**Imagick：：rotationalBlurImage()**函数是 PHP 中的一个内置函数，用于以特定角度将模糊应用于图像。

**语法：**

```php
*bool* Imagick::rotationalBlurImage( $angle, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$angle：**此参数用于存储角度的值。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道为**Imagick：：Channel_Default**。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：rotationalBlurImage()**函数：

**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

**程序 1：**

```php
<?php 

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use rotationalBlurImage function
$imagick->rotationalBlurImage(1);
$imagick->rotationalBlurImage(7);
$imagick->rotationalBlurImage(3);

// Set Image Header
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3a00e31537e41c1e4bab757a22869901.png)

**程序 2：**

```php
<?php 

// require_once('path/vendor/autoload.php');

// Create new Imagick Object
$imagick = new Imagick('
https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use rotationalBlurImage function
$imagick->rotationalBlurImage(6, 4);

// Set header image
header("Content-Type: image/jpg");

echo $imagick->getImageBlob();
?>
```

**输出：**
![rotationalImage1](img/b0ecd7073ee25f775018fffb6ed04a0a.png)

**引用：**[http://php.net/manual/en/imagick.rotationalblurimage.php](http://php.net/manual/en/imagick.rotationalblurimage.php)