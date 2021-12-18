# PHP|ImagickPixel setColorValue()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-setcolorvalue-function/](https://www.geeksforgeeks.org/php-imagickpixel-setcolorvalue-function/)

**ImagickPixel：：setColorValue()函数**是 PHP 中的一个内置函数，用于为给定 ImagickPixel 的颜色设置所提供颜色通道的规格化值。 规格化值是介于 0 和 1 之间的浮点数。

**语法：**

```
*bool* ImagickPixel::setColorValue( *int* $color, *float* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$color：**它指定[颜色常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.color-black)。
    所有颜色常量列表如下：
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   图像：：COLOR_BLUE(12)
    *   Imagick：：COLOR_ 青色(13)
    *   Imagick：：COLOR_GREEN(14)
    *   发布帖子：：COLOR_Red(15)
    *   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
    *   图像：：COLOR_MAGIC(17)
    *   Imagick：：color_opacity(18)
    *   Imagick：：COLOR_Alpha(19)
    *   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
*   **$value：**指定要设置的值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixel：：setColorValue()函数**：

**程序 1：**

```
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the color value
$imagickPixel->setColorValue(imagick::COLOR_RED, 0.8);

// Get the Color value with imagick::COLOR_RED
$colorValue = $imagickPixel->getColorValue(imagick::COLOR_RED);
echo $colorValue;
?>
```

发帖主题：Re：Колибри0.7.0

```
0.8
```

**程序 2：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator to iterate through each pixel
$imageIterator = $imagick->getPixelIterator();

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {
    // Loop through the pixels in the row
    if ($row % 5) {
        foreach ($pixels as $column => $pixel) {
            if ($column % 1000) {
                // Set the color
                $pixel->setColor("green");

                // Set the color value of Imagick::COLOR_ALPHA (opacity)
                $pixel->setColorValue(Imagick::COLOR_ALPHA, 0);
            }
        }
    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}

header("Content-Type: image/jpg");
echo $imagick;
?>
```

**输出：**
![](img/2d204edeec5e0c8401f74d6286b67cc1.png)

**引用：**[https://www.php.net/manual/en/imagickpixel.setcolorvalue.php](https://www.php.net/manual/en/imagickpixel.setcolorvalue.php)