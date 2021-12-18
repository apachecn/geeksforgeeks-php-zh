# PHP|Imagick parseColorImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-sparsecolorimage-function/](https://www.geeksforgeeks.org/php-imagick-sparsecolorimage-function/)

**Imagick：：parseColorImage()函数**是 PHP 中的一个内置函数，用于对整个图像中的颜色进行插值。

**语法：**

```php
*bool* Imagick::sparseColorImage( *int* $SPARSE_METHOD, *array* $arguments, *int* $channel )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$parse_method：**它指定与[SPARSECOLORMETHOD 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.sparsecolormethod-undefined)之一相对应的整数。 SPARSECOLORMETHOD 常量列表如下：
    *   Imagick：：SPARSECOLORMETHOD_UNDEFINED(0)
    *   Imagick：：SPARSECOLORMETHOD_ 重心(1)
    *   Imagick：：SPARSECOLORMETHOD_BILINEAR(7)
    *   Imagick：：SPARSECOLORMETHOD_PERMULATION(8)
    *   Imagick：：SPARSECOLORMETHOD_SPEPARDS(16)
    *   Imagick：：SPARSECOLORMETHOD_Voronoi(18)
*   **$参数：**它指定坐标。
*   **$channel(可选)：**它指定对您的通道模式有效的任何通道常量。 要应用多个通道，请使用按位运算符组合通道常量。 其默认值为 Imagick：：Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**Imagick：：parseColorImage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$array = array(0, 0, 1, 0, 0, 1, 900, 0, 0, 1,
               0, 1, 0, 1, 100, 1, 0, 70, 400,
               90, 0, 0, 1, 1);

// Apply the sparseColorImage() function
$imagick->sparseColorImage(imagick::SPARSECOLORMETHOD_BILINEAR, $array);

// Show the output
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/c31fdf30affd6508555af6078e809113.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$array = array(0, 0, 1, 0, 0, 1, 78, 0, 0, 1,
               0, 1, 0, 1, 10, 1, 0, 20, 400,
               90, 0, 0, 1, 1);

// Apply the sparseColorImage() function
$imagick->sparseColorImage(imagick::SPARSECOLORMETHOD_BARYCENTRIC, $array);

// Show the output
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/560b01925c6ab7a5703bbe0fdf6cdce9.png)

**引用：**[https://www.php.net/manual/en/imagick.sparsecolorimage.php](https://www.php.net/manual/en/imagick.sparsecolorimage.php)