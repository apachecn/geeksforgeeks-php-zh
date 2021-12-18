# PHP|Imagick NegateImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-negateimage-function/](https://www.geeksforgeeks.org/php-imagick-negateimage-function/)

**Imagick：：NegateImage()**函数是 PHP 中的一个内置函数，用于对参考图像中的颜色求反。 灰度选项意味着只有图像中的灰度值被取反。

**语法：**

```php
*bool* Imagick::negateImage( $gray, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$GREAY：**此参数用于设置仅否定图像中的灰度像素。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道是 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：NegateImage()**函数：

**程序：**

```php
<?php

// Create an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use negateImage function
$imagick->negateImage('true');

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![negate image](img/bc6ce28d5fd9b675cd47ef1d3fe9e3a6.png)

**相关文章：**

*   [PHP|Imagick blurImage()函数](https://www.geeksforgeeks.org/php-imagick-blurimage-function/)
*   [PHP|Imagick 转换 ImageColorspace()函数](https://www.geeksforgeeks.org/php-imagick-transformimagecolorspace-function/)

**引用：**[http://php.net/manual/en/imagick.negateimage.php](http://php.net/manual/en/imagick.negateimage.php)