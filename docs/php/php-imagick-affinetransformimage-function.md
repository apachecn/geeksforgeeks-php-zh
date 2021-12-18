# PHP|Imagick affineTransformImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-affinetransformimage-function/](https://www.geeksforgeeks.org/php-imagick-affinetransformimage-function/)

**Imagick：：affineTransformImage()函数**是 PHP 中的一个内置函数，用于根据仿射矩阵转换图像。

**语法：**

```
*bool* Imagick::affineTransformImage( $matrix )

```

**参数：**此函数接受单个参数**$matrix**，该参数保存仿射矩阵的值，可以基于旋转、SHEER、SCALE 等，…

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 Imagick：：affineTransformImage()函数：

**程序：**此程序使用 Imagick：：affineTransformImage()函数通过仿射给定的仿射矩阵来变换图像。

```
<?php

// Create an Imagick object
$imagick = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Create an ImagickDraw object
$imagickDraw = new \ImagickDraw();

// Set the angle
$theta = "35";

// Create affine transformation matrix
$affineRotate = array (
    "sx" => cos($theta), "sy" => cos($theta),
    "rx" => sin($theta), "ry" => -sin($theta),
    "tx" => 0, "ty" => 0,
);

// Use affine() function
$imagickDraw->affine($affineRotate);

// Set the image format
$imagick->setImageFormat("png");

// Use affineImageFormat() function
$imagick->affineTransformImage($imagickDraw);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![affineTransformImage() function](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**引用：**[https://www.php.net/manual/en/imagick.affinetransformimage.php](https://www.php.net/manual/en/imagick.affinetransformimage.php)