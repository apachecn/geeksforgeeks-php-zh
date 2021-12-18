# PHP|Imagick setImageWhitePoint()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagewhitepoint-function/](https://www.geeksforgeeks.org/php-imagick-setimagewhitepoint-function/)

**Imagick：：setImageWhitePoint()函数**是 PHP 中的内置函数，用于设置图像色度白点。

**语法：**

```php
*bool* Imagick::setImageWhitePoint( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定白点色度的 x 坐标。
*   **$y：**它指定白点色度的 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageWhitePoint()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the image white point
$imagick->setImageWhitePoint(0.65, 0.89);

// Get the image white point
$whitepoint = $imagick->getImageWhitePoint();
print("<pre>".print_r($whitepoint, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [x] => 0.65
    [y] => 0.89
)
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the image white point
$imagick->setImageWhitePoint(0.2, 0.2);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImagesBlob();
?>
```

**输出：**
![](img/fa3d4c6fb514828a171968d79364c5f4.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagewhitepoint.php](https://www.php.net/manual/en/imagick.setimagewhitepoint.php)