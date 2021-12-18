# PHP|Imagick resampleImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-resampleimage-function/](https://www.geeksforgeeks.org/php-imagick-resampleimage-function/)

**Imagick：：resampleImage()**函数是 PHP 中的内置函数，用于将图像重采样到所需的分辨率

**语法：**

```
*bool* Imagick::resampleImage( $x_resolution, $y_resolution, $filter, 
$blur )

```

**参数：**此函数接受上述四个参数，如下所述：

*   **$x_RESOLUTION：**此参数存储 x 分辨率的值。
*   **$y_Resolution：**此参数存储 y 分辨率的值。
*   **$filter：**此参数存储筛选器的值。
*   **$blur：**此参数存储模糊级别的值。

**返回值：**成功时此函数返回 True。
**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

下面的程序演示了 PHP 中的**Imagick：：resampleImage()**函数：

**程序：**

```
<?php    

// Create new Imagick object
$imagick = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use resampleImage function to resize image
$imagick->resampleImage(200, 200, \Imagick::FILTER_LANCZOS, 1);

// Image Header
header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/38591fcc28b9f4d63d73b74d91651892.png)

**引用：**[http://php.net/manual/en/imagick.resampleimage.php](http://php.net/manual/en/imagick.resampleimage.php)