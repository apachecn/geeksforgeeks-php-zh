# PHP|Imagick addNoiseImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagickaddnoiseimage-function/](https://www.geeksforgeeks.org/php-imagickaddnoiseimage-function/)

**Imagick：：addNoiseImage()**函数是 PHP 中的一个内置函数，用于在给定图像中添加噪声。 噪波的强度取决于噪波常数和通道类型。 图像噪声是图像中亮度和对比度的随机变化。

**语法：**

```
*bool* Imagick::addNoiseImage ( $noise_type, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$noise_type:** This parameter is used to set the noise types. There are some noise constants available in Imagick function which are listed below:
    *   Imagick：：Noise_Uniform
    *   Imagick：：Noise_Gauss
    *   Imagick：：Noise_MULTIPLICATIVEGAUSSIAN
    *   想象：：噪音 _ 脉冲
    *   Imagick：：Noise_Laplacian
    *   ==同步，由长者更正==
    *   Imagick：：Noise_Random

    ImageMagick 版本 6.3.6 及更高版本支持此常量。

*   **$channel：**此参数提供通道常量。 可以使用按位运算符组合两个或更多个通道。 Imagick 函数中有一些通道常量可用，如下所示：
    *   Imagick：：Channel_ 未定义
    *   Imagick：：Channel_red
    *   Imagick：：Channel_Gray
    *   Imagick：：Channel_Cyan
    *   Imagick：：Channel_Green
    *   Imagick：：Channel_Magenta
    *   Imagick：：Channel_Blue
    *   Imagick：：Channel_ 黄色
    *   Imagick：：Channel_Alpha
    *   Imagick：：Channel_Opacity
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   Imagick：：Channel_Black
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   Imagick：：Channel_Default

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：addNoiseImage()**函数：

**原图：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)
**程序：**

```
<?php 

// require_once('path/to/vendor/autoload.php'); 

header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$image->addNoiseImage(3, imagick::CHANNEL_DEFAULT);

echo $image;
?>
```

**输出：**
![](img/a0edfca835cba3ccfe8c6309dda65d17.png)

**引用：**[http://php.net/manual/en/imagick.addnoiseimage.php](http://php.net/manual/en/imagick.addnoiseimage.php)