# PHP|Imagick shearImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-shearimage-function/](https://www.geeksforgeeks.org/php-imagick-shearimage-function/)

**Imagick：：shearImage()**函数是 PHP 中的内置函数，用于创建平行四边形。 X 方向的剪切沿 X 轴滑动边，而 Y 方向的剪切沿 Y 轴滑动边。 剪切量由剪切角控制。

**语法：**

```php
*bool* Imagick::shearImage( $background, $x_shear, $y_shear )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$BACKGROUND：**此参数用于设置背景颜色。
*   **$x_shell：**此参数用于设置 x 轴上的剪切度数。
*   **$y_shear：**此参数用于设置沿 y 轴剪切的度数。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：shearImage()**函数：

**程序：**

```php
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use shearimage function
$imagick->shearimage('rgb(127, 127, 127)', 15, 5);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![shear image](img/363c40d1cb77a0f20a091e3404c89c9d.png)

**相关文章：**

*   [PHP|Imagick getImageHeight()函数](https://www.geeksforgeeks.org/php-imagick-getimageheight-function/)
*   [PHP|Imagick getImageWidth()函数](https://www.geeksforgeeks.org/php-imagick-getimagewidth-function/)

**引用：**[http://php.net/manual/en/imagick.shearimage.php](http://php.net/manual/en/imagick.shearimage.php)