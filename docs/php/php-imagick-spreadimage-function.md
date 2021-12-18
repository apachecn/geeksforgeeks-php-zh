# PHP|Imagick spreadImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-spreadimage-function/](https://www.geeksforgeeks.org/php-imagick-spreadimage-function/)

**Imagick：：spreadImage()**函数是 PHP 中的一个内置函数，它随机置换块中的每个像素。 它是一种特殊效果方法，可随机置换由 Radius 参数定义的块中的每个像素。

**语法：**

```
*bool* Imagick::spreadImage( $radius )
```

**参数：**此函数接受单个参数*$Radius*，该参数用于设置分配图像中每个像素的半径。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：spreadImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use spreadImage function
$imagick->spreadImage(5);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![spread image](img/c0df3bdbcf63a68e5814bd4847d32df0.png)

**相关文章：**

*   [PHP|Imagick getImageHeight()函数](https://www.geeksforgeeks.org/php-imagick-getimageheight-function/)
*   [PHP|Imagick getImageWidth()函数](https://www.geeksforgeeks.org/php-imagick-getimagewidth-function/)

**引用：**[http://php.net/manual/en/imagick.spreadimage.php](http://php.net/manual/en/imagick.spreadimage.php)