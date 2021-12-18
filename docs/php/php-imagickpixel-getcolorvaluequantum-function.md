# PHP|ImagickPixel getColorValueQuantum()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getcolorvaluequantum-function/](https://www.geeksforgeeks.org/php-imagickpixel-getcolorvaluequantum-function/)

**ImagickPixel：：getColorValueQuantum()函数**是 PHP 中的一个内置函数，用于获取给定 ImagickPixel 颜色的所提供颜色通道的归一化值。 与*getColorValue()*函数相反，归一化值位于量子范围内，其中 65535 为最大值，0 为最低值，其中 1 为最高值，0 为最低值。

**语法：**

```php
*int* ImagickPixel::getColorValueQuantum( *int* $color )
```

**参数：**此函数接受单个参数**$color**，该参数保存[个颜色常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.color-black)之一。

下面给出了所有颜色常量的列表：

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

**返回值：**此函数返回包含颜色值的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：getColorValueQuantum()函数**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel('#d4a62a');

// Get the Color value with imagick::COLOR_BLUE
$colorValue = $imagickPixel->getColorValueQuantum(imagick::COLOR_BLUE);
echo $colorValue;
?>
```

发帖主题：Re：Колибри0.7.0

```php
10794
```

**程序 2：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the 501th pixel
$getPixel = $histogramElements[500];

// Get the Color value with imagick::COLOR_GREEN
$colorValue = $getPixel->getColorValueQuantum(imagick::COLOR_GREEN);

echo $colorValue;
?>
```

发帖主题：Re：Колибри0.7.0

```php
26214
```

**引用：**[https://www.php.net/manual/en/imagickpixel.getcolorvaluequantum.php](https://www.php.net/manual/en/imagickpixel.getcolorvaluequantum.php)