# PHP|Imagick positeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-compositeimage-function/](https://www.geeksforgeeks.org/php-imagick-compositeimage-function/)

**Imagick：：CompositeImage()函数**是 PHP 中的一个内置函数，用于将一个图像合成到另一个图像中，并生成合成图像。

**语法：**

```
*bool* Imagick::compositeImage( $composite_object, $composite,
                       $x, $y, $channel = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$COMPOSITE_OBJECT：**它是一个 Imagick 对象，用于保存合成图像，也可以是要合成的图像的真实路径。
*   **$COMPOSITY：**它是一个复合运算符常量，如**Imagick：：COMPACTIVE_DEFAULT**、**Imagick：：COMPACTIVE_MATHORITHICS**等…
*   **x：**它保存合成图像的列偏移量。 **x**值将为数字格式。
*   **y：**它保持合成图像的行偏移量。 **y**值将为数字格式。
*   **$channel：**它有 Imagick 通道常量，可提供对您的通道模式有效的任何通道常量。 要应用多个通道，请使用按位运算符组合通道类型常量。

**返回值：**成功返回布尔值 True，失败返回布尔值 False。

下面的程序演示了 PHP 中的 Imagick：：CompositeImage()函数：

**程序：**

```
<?php

// Declare Imagick objects
$image1 = new \Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png");

$image2 = new \Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/negateImage.png");

// Resize the images
$image1->resizeimage($image2->getImageWidth(), 
        $image2->getImageHeight(), \Imagick::FILTER_LANCZOS, 1);

// Create new Imagick object
$new_image = new \Imagick();

// Create new image using ImageMagick pseudo-formats
$new_image->newPseudoImage($image1->getImageHeight(), 
        $image1->getImageWidth(), "gradient:gray(10%)-gray(90%)");

// Rotate the image
$new_image->rotateimage('black', 90);

// Use composite function to combined the image
$image2->compositeImage($new_image, \Imagick::COMPOSITE_COPYOPACITY, 0, 0);

// Use composite function to combined the image
$image1->compositeImage($image2, \Imagick::COMPOSITE_ATOP, 0, 0);

header("Content-Type: image/jpg");

// Display the output
echo $image1->getImageBlob();

?>
```

**输出：**
![](img/638d6c1ecff375bbf285e45f7fc93223.png)

**引用：**[https://www.php.net/manual/en/imagick.compositeimage.php](https://www.php.net/manual/en/imagick.compositeimage.php)