# PHP|Imagick equalizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-equalizeimage-function/](https://www.geeksforgeeks.org/php-imagick-equalizeimage-function/)

**Imagick：：equalizeImage()**函数是 PHP 中的一个内置函数，用于均衡图像的直方图。

**语法：**

```php
*bool* Imagick::equalizeImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/2aee72e5320a85a6e747db7b6fa1345f.png)

下面的程序演示了 PHP 中的**Imagick：：equalizeImage()**函数：

**程序：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

header('Content-type: image/png');

// Create an Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-16.png');

// Use equalizeImage function
$image->equalizeImage();

// Display output image
echo $image;
?>
```

**输出：**
![](img/2daad3a20db4233b7969dc299397114a.png)

**引用：**[http://php.net/manual/en/imagick.equalizeimage.php](http://php.net/manual/en/imagick.equalizeimage.php)