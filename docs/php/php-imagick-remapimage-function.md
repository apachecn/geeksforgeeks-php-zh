# PHP|Imagick remapImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-remapimage-function/](https://www.geeksforgeeks.org/php-imagick-remapimage-function/)

**Imagick：：reMapImage()函数**是 PHP 中的一个内置函数，用于将图像中的颜色替换为替换定义的颜色。 颜色将替换为尽可能接近的颜色。

**语法：**

```
*bool* Imagick::remapImage( *Imagick* $replacement, *int* $dither )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Replace：**它指定包含替换颜色的 Imagick 对象。
*   **$dither：**它指定与[DITHERMETHOD 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.dithermethod-undefined)之一相对应的整数值。 您也可以像*remapImage($Replace，Imagick：：DITHERMETHOD_Rimersma)；*那样直接传递常量。

所有 DITHERMETHOD 常量列表如下：

*   Imagick：：DITHERMETHOD_UNDEFINED(0)
*   Imagick：：DITHERMETHOD_NO(1)
*   Imagick：：DITHERMETHOD_RIMERSMA(2)
*   Imagick：：DITHERMETHOD_FLOYDSTEINBERG(3)

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：reMapImage()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create another Imagick object
$replacement = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191130231936/areplace.png');

// Remap the image
$imagick->remapImage($replacement, imagick::DITHERMETHOD_RIEMERSMA);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d7c563f249662450bc73e7343ab4b515.png)

**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Create another Imagick object
$replacement = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191130231936/areplace.png');

// Remap the image
$imagick->remapImage($replacement, imagick::DITHERMETHOD_FLOYDSTEINBERG);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/b206e3462461b77ad26b1dd59faf8c9d.png)

**引用：**[https://www.php.net/manual/en/imagick.remapimage.php](https://www.php.net/manual/en/imagick.remapimage.php)