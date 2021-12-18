# \\t0Ωphp|图像像素集 ColorValueQuantum()函数 __t1

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-setcolorvaluequantum-function/](https://www.geeksforgeeks.org/php-imagickpixel-setcolorvaluequantum-function/)

**ImagickPixel：：setColorValueQuantum()函数**是 PHP 中的一个内置函数，用于为给定 ImagickPixel 的颜色设置提供的颜色通道的值。 该值可以在 0 到 65535 的范围内。

**语法：**

```php
*bool* ImagickPixel::setColorValueQuantum( *int* $color, *float* $value )
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

下面给出的程序演示了 PHP 中的**ImagickPixel：：setColorValueQuantum()函数**：

**程序 1：**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the color value
$imagickPixel->setColorValueQuantum(imagick::COLOR_BLUE, 4500);

// Get the Color value with imagick::COLOR_BLUE
$colorValue = $imagickPixel->getColorValueQuantum(imagick::COLOR_BLUE);
echo $colorValue;
?>
```

发帖主题：Re：Колибри0.7.0

```php
4500
```

**程序 2：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator to iterate through each pixel
$imageIterator = $imagick->getPixelIterator();
$x = 200;

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {
    // Loop through the pixels in the row
    if ($row % 2) {
        foreach ($pixels as $column => $pixel) {
            if ($column % 1000) {
                // Set the color
                $pixel->setColor("red");

                // Set the color value of Imagick::COLOR_RED
                $pixel->setColorValueQuantum(Imagick::COLOR_RED, $x);
                $x = $x + 1000;
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
![](img/b10d9e29669279addd0865644ec0e666.png)

**引用：**[https://www.php.net/manual/en/imagickpixel.setcolorvaluequantum.php](https://www.php.net/manual/en/imagickpixel.setcolorvaluequantum.php)