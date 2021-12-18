# PHP|Imagick oilPaintImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-oilpaintimage-function/](https://www.geeksforgeeks.org/php-imagick-oilpaintimage-function/)

**Imagick：：oilPaintImage()**函数是 PHP 中的内置函数，用于模拟油画。 此函数应用模拟油画的特殊效果滤镜。 此函数用半径定义的圆形区域中出现的最频繁的颜色替换每个像素。

**语法：**

```
*bool* Imagick::oilPaintImage( $radius )
```

**参数：**此函数接受单个参数*$Radius*。 用于设置圆形邻域的半径。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：oilPaintImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use oilPaintImage function
$imagick->oilPaintImage(5);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![oil paint image](img/647ee7c9807d94b550f1910306da94c5.png)

**引用：**[http://php.net/manual/en/imagick.oilpaintimage.php](http://php.net/manual/en/imagick.oilpaintimage.php)