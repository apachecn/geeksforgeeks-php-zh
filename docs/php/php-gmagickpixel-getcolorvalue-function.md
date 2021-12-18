# PHP|GmagickPixel getColorvalue()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickpixel-getcolorvalue-function/](https://www.geeksforgeeks.org/php-gmagickpixel-getcolorvalue-function/)

**GmagickPixel：：getColorvalue()函数**是 PHP 中的一个内置函数，用于获取给定 GmagickPixel 颜色的所提供颜色通道的归一化值。 规格化值是介于 0 和 1 之间的浮点数。

**语法：**

```
*float* GmagickPixel::getcolorvalue( *int* $color )
```

**参数：**此函数接受单个参数**$color**，该参数保存与[颜色常量](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.color-black)之一相对应的整数值。
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

**返回值：**此函数返回指定为 0 到 1 之间的浮点数的颜色通道的值。

**异常：**此函数在出错时引发 GmagickPixelException。

下面给出的程序演示了 PHP 中的**GmagickPixel：：getColorvalue()函数**：

**程序 1：**

```
<?php 

// Create a new gmagickPixel object 
$gmagickPixel = new GmagickPixel('#ad4c45'); 

// Get the Color value with imagick::COLOR_RED 
$colorValue = $gmagickPixel->getcolorvalue(gmagick::COLOR_RED); 
echo $colorValue; 
?>
```

发帖主题：Re：Колибри0.7.0

```
0.67843137254902
```

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image histogram 
$histogramElements = $gmagick->getimagehistogram(); 

// Get the 301th pixel 
$getPixel = $histogramElements[300]; 

// Get the Color value with gmagick::COLOR_GREEN 
$colorValue = $getPixel->getcolorvalue(gmagick::COLOR_GREEN); 

echo $colorValue; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
0.29803921568627
```

**引用：**[https://www.php.net/manual/en/gmagickpixel.getcolorvalue.php](https://www.php.net/manual/en/gmagickpixel.getcolorvalue.php)