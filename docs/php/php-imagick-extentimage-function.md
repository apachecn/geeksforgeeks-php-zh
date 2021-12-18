# PHP|Imagick extentImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-extentimage-function/](https://www.geeksforgeeks.org/php-imagick-extentimage-function/)

**Imagick：：extentImage()**函数是 PHP 中的内置函数，它提供了设置图像大小的方法。 此方法设置图像大小，并允许设置图像新区域开始处的 x，y 坐标。

**语法：**

```
*bool* Imagick::extentImage( $width, $height, $x, $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width：**此参数存储新宽度的值。
*   **$Height：**此参数存储新高度的值。
*   **$x：**此参数存储新大小的 X 位置的值。
*   **$y：**此参数存储新大小的 Y 位置的值。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f3f9ad737830ec5f484ea0965e65694b.png)

下面的程序演示了 PHP 中的**Imagick：：extentImage()**函数：

**程序：**

```
<?php 

/*require_once('path/vendor/autoload.php');*/

/*Imagick Object*/
$image = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png');

/*Set Background Color*/
$image->setImageBackgroundColor('orange');

/*extentImage*/

$image->extentImage(
    $image->getImageWidth(),
    $image->getImageHeight(),
    -100,
    -100
);

/*Image Header*/
header("Content-Type: image/jpg");

// Display output image
echo $image->getImageBlob();
?>
```

**输出：**
![](img/0fbefd6fbb19f9ac61980d4f2bb02623.png)

**引用：**[http://php.net/manual/en/imagick.extentimage.php](http://php.net/manual/en/imagick.extentimage.php)