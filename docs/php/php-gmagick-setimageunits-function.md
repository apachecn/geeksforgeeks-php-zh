# PHP|Gmagick setimageunit()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimageunits-function/](https://www.geeksforgeeks.org/php-gmagick-setimageunits-function/)

**gmagick：：setimageunit()函数**是 PHP 中的一个内置函数，用于设置特定图像的分辨率单位。 此函数对图像没有视觉影响，但只更改分辨率单位，可以是未定义分辨率、PixelsPerInchResolution 或 PixelsPerCentimeterResolution 之一。

**语法：**

```php
*Gmagick* Gmagick::setimageunits( *int* $resolution )
```

**参数：**此函数接受单个参数**$Resolution**，该参数保存与[分辨率常量](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.resolution-undefined)之一相对应的整数。

下面给出了所有分辨率常量的列表：

*   Gmagick：：RESOLUTION_UNDEFINED(0)
*   Gmagick：：RESOLUTION_PIXELSPERINCH(1)
*   Gmagick：：RESOLUTION_PIXELSPERCENTIMETER(2)

**返回值：**此函数在成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimageunit()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image units
$gmagick->setImageUnits(Gmagick::RESOLUTION_PIXELSPERCENTIMETER);

// Get the image units
$units = $gmagick->getimageunits();
echo $units;
?>
```

发帖主题：Re：Колибри0.7.0

```php
2  // Which corresponds to Gmagick::RESOLUTION_PIXELSPERCENTIMETER
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image units
$gmagick->setImageUnits(Gmagick::RESOLUTION_PIXELSPERINCH);

// Display the image using new units
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/1c345e18ea7920bea8e11476e08ad796.png)

**引用：**[https://www.php.net/manual/en/gmagick.setimageunits.php](https://www.php.net/manual/en/gmagick.setimageunits.php)