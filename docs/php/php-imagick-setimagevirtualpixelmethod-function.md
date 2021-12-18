# PHP|Imagick setImageVirtualPixelMethod()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagevirtualpixelmethod-function/](https://www.geeksforgeeks.org/php-imagick-setimagevirtualpixelmethod-function/)

**Imagick：：setImageVirtualPixelMethod()函数**是 PHP 中的内置函数，用于设置图像虚拟像素方法。

**语法：**

```php
*bool* Imagick::setImageVirtualPixelMethod( *int* $method )
```

**参数：**此函数接受单个参数**$method**，该参数包含与[VIRTUALPIXELMETHOD 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.virtualpixelmethod-undefined)之一相对应的整数值。 我们也可以像*setImageVirtualPixelMethod(imagick：：VIRTUALPIXELMETHOD_BLACK)；*那样直接传递常量。

所有 VIRTUALPIXELMETHOD 常量如下：

*   Imagick：：VIRTUALPIXELMETHOD_UNDEFINED(0)
*   Imagick：：VIRTUALPIXELMETHOD_BACKGROUND(1)
*   Imagick：：VIRTUALPIXELMETHOD_CONSTANTER(2)
*   Imagick：：VIRTUALPIXELMETHOD_CONSTANTER(2)
*   想象：VIRTUALPIXELMETHOD_THREACTOR(8)
*   Imagick：：VIRTUALPIXELMETHOD_MASK(9)
*   Imagick：：VIRTUALPIXELMETHOD_BLACK(10)
*   Imagick：：VIRTUALPIXELMETHOD_Gray(11)
*   Imagick：：VIRTUALPIXELMETHOD_Gray(11)
*   Imagick：

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setImageVirtualPixelMethod()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Virtual Pixel Method
$imagick->setImageVirtualPixelMethod(imagick::VIRTUALPIXELMETHOD_BLACK);

// Get the Virtual Pixel Method
$virtualPixelMethod = $imagick->getImageVirtualPixelMethod();
echo $virtualPixelMethod;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Virtual Pixel Method
$imagick->setImageVirtualPixelMethod(imagick::VIRTUALPIXELMETHOD_TILE);

// Get the Virtual Pixel Method
$virtualPixelMethod = $imagick->getImageVirtualPixelMethod();
echo $virtualPixelMethod;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimagevirtualpixelmethod.php](https://www.php.net/manual/en/imagick.setimagevirtualpixelmethod.php)