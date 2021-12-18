# PHP|Imagick 形态学()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-morphology-function/](https://www.geeksforgeeks.org/php-imagick-morphology-function/)

**Imagick：：Sphology()函数**是 PHP 中的一个内置函数，用于根据给定的形态学方法将用户提供的内核应用于图像。
**语法：**

```
*bool* Imagick::morphology
( $morphologyMethod, $iterations, $ImagickKernel, $channel = Imagick::CHANNEL_DEFAULT)
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$formologyMethod：**此参数保存要使用的形态学方法。
*   **$iterations：**此参数保存要应用形态学函数的迭代次数。
*   **$ImagickKernel：**此参数保存 ImagickKernel 对象。
*   **$channel：**此参数保存 Imagick 通道常量，这些常量提供对通道模式有效的任何通道常量。 可以使用按位运算符组合多个通道。 默认值为 Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。
**异常：**此函数在出错时引发 ImagickException。
下面的程序说明了 PHP 中的**Imagick：：Sphology()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Create a ImagickKernel object
$kernel = ImagickKernel::fromBuiltIn(Imagick::KERNEL_DIAMOND, "2");

// Apply the morphology function
$imagick->morphology(Imagick::MORPHOLOGY_CONVOLVE, 2, $kernel);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/69cf598f40f079af2ae15e800d3454d7.png)
**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Create a ImagickKernel object
$kernel = ImagickKernel::fromBuiltIn(Imagick::KERNEL_GAUSSIAN, "1, 2");

// Apply the morphology function
$imagick->morphology(Imagick::MORPHOLOGY_CONVOLVE, 5, $kernel);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/a1385aa0e9244011988aebe9ce20cd87.png)
**参考：**[https://www.php.net/manual/en/imagick.morphology.php](https://www.php.net/manual/en/imagick.morphology.php)