# PHP|Imagick implodeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-implodeimage-function/](https://www.geeksforgeeks.org/php-imagick-implodeimage-function/)

**Imagick implodeImage()函数**是 PHP 中的一个内置函数，用于创建一个新图像作为副本。

**语法：**

```php
*bool* Imagick::implodeImage( $radius )
```

**参数：**此函数接受保存内爆半径的单个参数**半径**。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick implodeImage()函数：

**程序：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use Imagick::implodeImage() function to the image
$imagick->implodeImage(0.0001);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![Imagick::implodeImage](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**引用：**[https://www.php.net/manual/en/imagick.implodeimage.php](https://www.php.net/manual/en/imagick.implodeimage.php)