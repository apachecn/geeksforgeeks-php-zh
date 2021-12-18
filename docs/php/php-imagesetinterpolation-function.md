# PHP|imagesetinterpolation()函数

> Original: [https://www.geeksforgeeks.org/php-imagesetinterpolation-function/](https://www.geeksforgeeks.org/php-imagesetinterpolation-function/)

**imagesetinterpolation()函数**是 PHP 中内置的函数，用于设置插值方法，设置插值方法会影响各种函数的渲染，如*imagerotate()*函数。
**语法：**和

```
*bool* imagesetinterpolation( *resource* $image, *int* $method )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$method：**指定要应用的方法。(
    可用方法列表如下：
    *   Img_Bell：贝尔过滤器。
    *   Img_bessel：贝塞尔过滤器。
    *   Img_BICUBIC：双三次插值。
    *   Img_BICUBIC_FIXED：双三次插值的定点实现。
    *   IMG_BILINEAR_FIXED：双线性插值的定点实现(默认(也适用于图像创建))。
    *   Img_Blackman：Blackman 窗口函数。
    *   Img_box：长方体模糊滤镜。
    *   Img_BSPLINE：样条插值。
    *   IMG_CATMULLROM：三次 Hermite 样条插值。
    *   Img_uss：高斯函数。
    *   Img_ 广义 _ 立方：广义三次样条分形插值。
    *   Img_HERMITE：Hermite 插值。
    *   Img_hamming：汉明滤波器。
    *   Img_hning：汉宁过滤器。
    *   Img_Mitchell：Mitchell 过滤器。
    *   Img_power：幂插值。
    *   Img_QUADATIC：反二次插值。
    *   Img_SINC：sinc 函数。
    *   Img_NEAREST_RENERSOUR：最近邻居插值。
    *   IMG_WEIGHTED4：加权过滤器。
    *   Img_triangle：三角形插值。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。
以下示例说明 PHP 中的**imagesetinterpolation()函数**：
**示例 1：**和

## PHP

```
<?php

// Load the png image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the interpolation
imagesetinterpolation($image, IMG_BLACKMAN);

// Rotate the image
$black = imagecolorallocate($image, 0, 0, 0);
$rotated = imagerotate($image, 20, $black);

// Output image to the browser
header('Content-type: image/png');
imagepng($rotated);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/fecd7a18a34ac5864224aa9e757107a8.png)

**示例 2：**和

## PHP

```
<?php

// Load the png image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the interpolation
imagesetinterpolation($image, IMG_POWER);

// Rotate the image
$black = imagecolorallocate($image, 0, 0, 0);
$rotated = imagerotate($image, 20, $black);

// Output image to the browser
header('Content-type: image/png');
imagepng($rotated);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/d7b3bc03207a6426fa5c13f23dd43a91.png)

**引用：**[https://www.php.net/manual/en/function.imagesetinterpolation.php](https://www.php.net/manual/en/function.imagesetinterpolation.php)