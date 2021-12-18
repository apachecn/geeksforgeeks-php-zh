# PHP|Imagick QuantizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-quantizeimage-function/](https://www.geeksforgeeks.org/php-imagick-quantizeimage-function/)

**Imagick：：QuantizeImage()函数**是 PHP 中的一个内置函数，用于分析参考图像中的颜色。

**语法：**

```
*bool* Imagick::quantizeImage ( *int* $numberColors, *int* $colorspace, 
*int* $treedepth, *bool* $dither, *bool* $measureError)
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$numColors：**它指定颜色的数量。
*   **$Colorspace：**它指定颜色空间。
*   **$TreeDepth：**它指定树的深度。
*   **$dither：**它指定是否启用抖动。
*   **$measure Error：**指定是否启用误差测量。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：QuantizeImage()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Quantize the Image
$imagick->quantizeImage(100, 8, 256, true, false);

// Display the image
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/7019f9d821d8f58a88ec53d1c389cd9a.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Quantize the Image
$imagick->quantizeImage(2, 50, 256, true, false);

// Display the image
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/1171fa992e44b16b8c1b84801ca49b7e.png)

**引用：**[https://www.php.net/manual/en/imagick.quantizeimage.php](https://www.php.net/manual/en/imagick.quantizeimage.php)