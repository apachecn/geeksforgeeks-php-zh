# PHP|Imagick edgeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-edgeimage-function/](https://www.geeksforgeeks.org/php-imagick-edgeimage-function/)

**Imagick：：edgeImage()**函数是 PHP 中的内置函数，用于增强图像中的边缘。 它在给定半径的卷积滤波器的帮助下增强边缘。

**语法：**

```
*bool* Imagick::edgeImage( $radius )
```

**参数：**此函数接受单个参数*$Radius*，该参数用于存储半径的值。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/2aee72e5320a85a6e747db7b6fa1345f.png)

下面的程序说明了 PHP：
**程序：**中的**Imagick：：edgeImage()**函数

```
<?php 

// require_once('path/vendor/autoload.php'); 

// header('Content-type: image/png');

// Create an Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-16.png');

// Use edgeImage function
$image->edgeImage(2);

// Display output image
echo $image;
?>
```

**输出：**
![](img/756ba8326e76c82a5bd84b3e3fb6eb7f.png)

**引用：**[http://php.net/manual/en/imagick.edgeimage.php](http://php.net/manual/en/imagick.edgeimage.php)