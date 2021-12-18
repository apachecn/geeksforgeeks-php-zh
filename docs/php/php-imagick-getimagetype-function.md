# PHP|Imagick getImageType()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagetype-function/](https://www.geeksforgeeks.org/php-imagick-getimagetype-function/)

**Imagick：：getImageType()函数**是 PHP 中的一个内置函数，用于获取潜在的图像类型。

**语法：**

```
*int* Imagick::getImageType( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与 IMGTYPE 常量之一对应的整数值。

下面列出了所有 IMGTYPE 常量：

*   Imagick：：IMGTYPE_UNDEFINED(0)
*   Imagick：：IMGTYPE_BILLEVEL(1)
*   Imagick：：IMGTYPE_GRAYSCALE(2)
*   Imagick：：IMGTYPE_GRAYSCALEMATTE(3)
*   Imagick：：IMGTYPE_Palette(4)
*   Imagick：：IMGTYPE_Palettematte(5)
*   Imagick：：IMGTYPE_TRUECOLOR(6)
*   Imagick：：IMGTYPE_TRUECOLORMATTE(7)
*   Imagick：：IMGTYPE_COLORSEPARATION(8)
*   Imagick：：IMGTYPE_COLORSEPARATIONMATTE(9)
*   Imagick：：IMGTYPE_OPTIMIZE(10)

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getImageType()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Image Type
$type = $imagick->getImageType();
echo $type;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Type
$imagick->setImageType(3);

// Get the Image Type
$type = $imagick->getImageType();
echo $type;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagetype.php](https://www.php.net/manual/en/imagick.getimagetype.php)