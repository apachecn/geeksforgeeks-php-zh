# PHP|Imagick getImageInterpolateMethod()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageinterpolatemethod-function/](https://www.geeksforgeeks.org/php-imagick-getimageinterpolatemethod-function/)

**Imagick：：getImageInterpolateMethod()函数**是 PHP 中的内置函数，用于获取指定图像的插值方法。

**语法：**

```php
*int* Imagick::getImageInterpolateMethod( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，其中包含与某个插值常量对应的插值方法。

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

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：getImageInterpolateMethod()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Interpolate Method
$interpolateScheme = $imagick->getImageInterpolateMethod();
echo $interpolateScheme
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interpolate Method
$imagick->setImageInterpolateMethod(imagick::INTERPOLATE_MESH);

// Get the Interpolate Method
$interpolateScheme = $imagick->getImageInterpolateMethod();
echo $interpolateScheme;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageinterpolatemethod.php](https://www.php.net/manual/en/imagick.getimageinterpolatemethod.php)