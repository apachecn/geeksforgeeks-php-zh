# PHP|Imagick deseckleImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-despeckleimage-function/](https://www.geeksforgeeks.org/php-imagick-despeckleimage-function/)

**Imagick：：deseckleImage()**函数是 PHP 中的一个内置函数，用于减少图像中的斑点噪声，同时保留原始图像的边缘。

**语法：**

```
*bool* Imagick::despeckleImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f3f9ad737830ec5f484ea0965e65694b.png)

下面的程序演示了 PHP 中的 I**magick：：deseckleImage()**函数：

**程序：**

```
<?php 
/*require_once('path/vendor/autoload.php');*/ 

/*Imagick Object*/
$image = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png');

/*despeckleImage Image*/
$image->despeckleImage();

/*Image Header*/
header("Content-Type: image/jpg");

// Display output image
echo $image;
?>
```

**输出：**
![](img/eb1b56c582f6d77d1cd2dbc8e6dbeccb.png)

**引用：**[http://php.net/manual/en/imagick.despeckleimage.php](http://php.net/manual/en/imagick.despeckleimage.php)