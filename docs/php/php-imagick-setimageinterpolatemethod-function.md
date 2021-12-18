# PHP|Imagick setImageInterpolateMethod()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageinterpolatemethod-function/](https://www.geeksforgeeks.org/php-imagick-setimageinterpolatemethod-function/)

**Imagick：：setImageInterpolateMethod()函数**是 PHP 中的内置函数，用于设置图像的隔行扫描方案。

**语法：**

```
*bool* Imagick::setImageInterpolateMethod( *int* $method )
```

**参数：**此函数接受单个参数**$method**，该参数对应于[插值常数](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.interpolate-undefined)之一。 我们也可以像
*setImageInterpolateMethod(imagick：：INTERPOLATE_BICUBIC)；*那样直接传递常量。

插补常量列表如下：

*   Imagick：：Interpolate_UNDEFINED(0)
*   Imagick：：Interpolate_Average(1)
*   Imagick：：Interpolate_BICUBIC(2)
*   Imagick：：插值 _ 双线性(3)
*   Imagick：：Interpolate_Filter(4)
*   Imagick：：Interpolate_Integer(5)
*   Imagick：：Interpolate_Mesh(6)
*   Imagick：：Interpolate_NEARESTNEIGHBOR(7)
*   Imagick：：Interpolate_Spline(8)

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setImageInterpolateMethod()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interpolate Method
$imagick->setImageInterpolateMethod(imagick::INTERPOLATE_BILINEAR);

// Get the Interpolate Method
$interpolateScheme = $imagick->getImageInterpolateMethod();
echo $interpolateScheme;
?>
```

发帖主题：Re：Колибри0.7.0

```
3 // Which corresponds to imagick::INTERPOLATE_BILINEAR.
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interpolate Method
$imagick->setImageInterpolateMethod(imagick::INTERPOLATE_NEARESTNEIGHBOR);

// Get the Interpolate Method
$interpolateScheme = $imagick->getImageInterpolateMethod();
echo $interpolateScheme;
?>
```

发帖主题：Re：Колибри0.7.0

```
7 // Which corresponds to imagick::INTERPOLATE_NEARESTNEIGHBOR.
```

**引用：**[https://www.php.net/manual/en/imagick.setimageinterpolatemethod.php](https://www.php.net/manual/en/imagick.setimageinterpolatemethod.php)