# PHP|Imagick zezeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-resizeimage-function/](https://www.geeksforgeeks.org/php-imagick-resizeimage-function/)

**Imagick：：ResizeImage()函数**是 PHP 中的一个内置函数，用于将图像缩放到所需的尺寸。

**语法：**

```
*bool* Imagick::resizeImage( *int* $columns, 
*int* $rows, *int* $filter, *float* $blur, 
*bool* $best_fit = false, *bool* $legacy = false )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$Columns：**它指定图像的宽度。
*   **$ROWS：**它指定图像的高度。
*   **$filter：**它指定与[过滤常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.filter-undefined)之一相对应的整数。
*   **$blur：**它指定模糊因子，其中>1 为模糊，<1 为锐化。
*   **$BEST_FIT(可选)：**它指定 FIT 参数。
*   **$Legacy(可选)：**它指定传统。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：ResizeImage()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Resize the image
$imagick->resizeImage( 620, 300, Imagick::FILTER_LANCZOS, 1);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/1563d267ef807c50bed05a11ef1f4978.png)

**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Resize the image
$imagick->resizeImage( 520, 200, imagick::FILTER_GAUSSIAN, 10);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/cca83724d52df3edad37ebad80975257.png)

**引用：**[https://www.php.net/manual/en/imagick.resizeimage.php](https://www.php.net/manual/en/imagick.resizeimage.php)