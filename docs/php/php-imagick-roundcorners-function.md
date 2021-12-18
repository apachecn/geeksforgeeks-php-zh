# PHP|Imagick round Corners()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-roundcorners-function/](https://www.geeksforgeeks.org/php-imagick-roundcorners-function/)

**Imagick：：round Corners()函数**是 PHP 中的一个内置函数，用于对图像角点进行圆角处理。

**语法：**

```php
*bool* Imagick::roundCorners( *float* $x_rounding, 
*float* $y_rounding, *float* $stroke_width = 10, 
*float* $displace = 5, *float* $size_correction = -6 )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$x_ROUNDING：**它指定 x 舍入量。
*   **$y_round ding：**它指定 y 舍入量。
*   **$STROCK_WIDTH(可选)：**它指定笔划宽度。 该参数的默认值为 10。
*   **$displace(可选)：**它指定图像位移。 该参数的默认值为 5。
*   **$SIZE_RECORATION(可选)：**它指定大小校正。 该参数的默认值为-6。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：round Corners()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Round the corners
$imagick->roundCorners(20, 20, 5, 5, -8);

// Display the image
$imagick->setImageFormat('jpg');
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/dd4dea7aaed22613766dc9fba2a34001.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Round the corners
$imagick->roundCorners(100, 100, 5);

// Display the image
$imagick->setImageFormat('jpg');
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/7d36743556b67f65ee3400301cf92492.png)

**引用：**[https://www.php.net/manual/en/imagick.roundcorners.php](https://www.php.net/manual/en/imagick.roundcorners.php)