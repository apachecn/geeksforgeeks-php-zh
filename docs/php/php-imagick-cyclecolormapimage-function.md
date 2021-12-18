# PHP|Imagick cycleColormapImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-cyclecolormapimage-function/](https://www.geeksforgeeks.org/php-imagick-cyclecolormapimage-function/)

**Imagick：：cycleColormapImage()函数**是 PHP 中的一个内置函数，用于替换色彩映射表(它是一个 m×3 矩阵，包含介于 0.0 和 1.0 之间的实数。 矩阵的每一行都是定义一种颜色的 RGB 矢量。)。 通过给定数量的位置来调整图像的大小。 如果你循环使用色彩映射表的次数，那么它会产生一种迷幻效果。

**语法：**

```
*bool* Imagick::cycleColormapImage( $displace )
```

**参数：**此函数接受单个参数**$displace**，该参数保存置换颜色贴图的量(整数)。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的 Imagick：：cycleColormapImage()函数：

**程序：**

```
<?php

// Declare an Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Use Imagick::cycleColormapImage() function
$image->cycleColormapImage (8);

header("Content-Type: image/jpg"); 

// Display the output image
echo $image->getImageBlob();

?>
```

**输出：**
![](img/04f604bde1c6ff0c7cd9042a259271f4.png)

**引用：**[https://www.php.net/manual/en/imagick.cyclecolormapimage.php](https://www.php.net/manual/en/imagick.cyclecolormapimage.php)