# PHP|Imagick QuantizeImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-quantizeimages-function/](https://www.geeksforgeeks.org/php-imagick-quantizeimages-function/)

**Imagick：：QuantizeImages()函数**是 PHP 中的一个内置函数，用于分析图像序列中的颜色。 这通常对 gif 动画很有帮助。

**语法：**

```
*bool* Imagick::quantizeImages(*int* $numberColors, *int* $colorspace,
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

下面给出的程序演示了 PHP 中的**Imagick：：QuantizeImages()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// Quantize the Image
$imagick->quantizeImages(2, 50, 256, true, false);

// Display the image
$imagick->setImageFormat('gif');
header("Content-Type: image/gif");
echo $imagick->getImagesBlob();
?>
```

**输出：**
![](img/83b6f64c531c089abd8c79ecd01f9820.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif');

// Quantize the Image
$imagick->quantizeImages(2, 80, 256, true, false);

// Display the image
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImagesBlob();
?>
```

**输出：**
![](img/30aba1f9579595f63686e56adefd31f9.png)

**引用：**[https://www.php.net/manual/en/imagick.quantizeimages.php](https://www.php.net/manual/en/imagick.quantizeimages.php)