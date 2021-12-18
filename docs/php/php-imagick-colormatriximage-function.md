# PHP|Imagick color MatrixImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-colormatriximage-function/](https://www.geeksforgeeks.org/php-imagick-colormatriximage-function/)

**Imagick：：ColorMatrixImage()函数**是 PHP 中的一个内置函数，用于将颜色转换应用于图像。 此函数会导致饱和度变化、色调旋转、亮度变为 Alpha 以及各种其他效果。 此函数使用可变大小的变换矩阵，即**RGBA**使用**5×5**矩阵，**CMYKA**使用**6×6**矩阵。

**语法：**

```php
*bool* Imagick::colorMatrixImage( array $color_matrix = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受单个参数**$COLOR_MATRIX**，该参数用于保存 RGBA 的 5×5 矩阵，行表示红、绿、蓝、阿尔法输出，列为红、绿、蓝、阿尔法输入，最后一行和列用于亮度调整。 在 CMYKA 的 6×6 矩阵中，行表示青色、洋红色、黄色、按键或黑色、阿尔法输出，列是青色、洋红色、黄色、按键或黑色、阿尔法输入，而类似于 RGBA 的用于亮度调整的阿尔法，CMYKA 也具有用于亮度调整的最后行和列。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 Imagick：：ColorMatrixImage()函数：

**程序：**

```php

<?php

// 6x6 color matrix for CMYKA
$colorMatrix = [
    1.5, 0.0, 0.0, 0.0, 0.0, -0.157,
    0.0, 0.0, 0.5, 0.0, 0.0, -0.157,
    0.0, 0.0, 0.0, 0.0, 0.5, -0.157,
    0.0, 0.0, 0.0, 1.0, 0.0,  0.0,
    0.0, 0.0, 0.0, 0.0, 1.0,  0.0,
    0.0, 0.0, 0.0, 0.5, 0.0,  1.0
];

// Create Imagick object 
$imagick = new \Imagick(
'https://cdncontribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set image opacity
$imagick->evaluateImage(
    Imagick::EVALUATE_MULTIPLY, 
    0.6, 
    Imagick::CHANNEL_ALPHA
);

// Create new Imagick object
$background = new \Imagick();

// Creating new pseudo image with hexagon pattern
$background->newPseudoImage(
    $imagick->getImageWidth(), 
    $imagick->getImageHeight(),  
    "pattern:hexagons"
);

// Set the image format
$background->setImageFormat('png');
$imagick->setImageFormat('png');

// Use Imagick::colorMatrixImage() function
$imagick->colorMatrixImage($colorMatrix);

// Use Imagick::compositeImage() function     
$background->compositeImage(
    $imagick, 
    \Imagick::COMPOSITE_SRCATOP,
    0,
    0
);

header("Content-Type: image/png");

// Display the output image
echo $background->getImageBlob();

?>
```

**输出：**
![](img/422fd2c607728e9d991ddbf49fb80971.png)

**引用：**[https://www.php.net/manual/en/imagick.colormatriximage.php](https://www.php.net/manual/en/imagick.colormatriximage.php)