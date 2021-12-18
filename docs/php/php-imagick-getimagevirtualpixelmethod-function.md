# PHP|Imagick getImageVirtualPixelMethod()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagevirtualpixelmethod-function/](https://www.geeksforgeeks.org/php-imagick-getimagevirtualpixelmethod-function/)

**Imagick：：getImageVirtualPixelMethod()函数**是 PHP 中的内置函数，用于获取图像虚拟像素方法。

**语法：**

```
*int* Imagick::getImageVirtualPixelMethod( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与[VIRTUALPIXELMETHOD 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.virtualpixelmethod-undefined)之一对应的整数值。

所有 VIRTUALPIXELMETHOD 常量如下：

*   Imagick：：VIRTUALPIXELMETHOD_UNDEFINED(0)
*   Imagick：：VIRTUALPIXELMETHOD_BACKGROUND(1)
*   Imagick：：VIRTUALPIXELMETHOD_CONSTANTER(2)
*   Imagick：：VIRTUALPIXELMETHOD_EDGE(4)
*   Imagick：：VIRTUALPIXELMETHOD_MIRROR(5)
*   Imagick：：VIRTUALPIXELMETHOD_TILE(7)
*   Imagick：：VIRTUALPIXELMETHOD_TH 透明(8)
*   Imagick：：VIRTUALPIXELMETHOD_MASK(9)
*   Imagick：：VIRTUALPIXELMETHOD_BLACK(10)
*   Imagick：：VIRTUALPIXELMETHOD_Gray(11)
*   Imagick：：VIRTUALPIXELMETHOD_ 怀特(12)
*   Imagick：：VIRTUALPIXELMETHOD_HORIZONTALTILE(13)
*   Imagick：：VIRTUALPIXELMETHOD_VERTICALTILE(14)

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageVirtualPixelMethod()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Virtual Pixel Method
$virtualPixelMethod = $imagick->getImageVirtualPixelMethod();
echo $virtualPixelMethod;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Virtual Pixel Method
$imagick->setImageVirtualPixelMethod(imagick::VIRTUALPIXELMETHOD_TRANSPARENT);

// Get the Virtual Pixel Method
$virtualPixelMethod = $imagick->getImageVirtualPixelMethod();
echo $virtualPixelMethod;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagevirtualpixelmethod.php](https://www.php.net/manual/en/imagick.getimagevirtualpixelmethod.php)