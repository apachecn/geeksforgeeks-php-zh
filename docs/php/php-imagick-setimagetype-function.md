# PHP|Imagick setImageType()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagetype-function/](https://www.geeksforgeeks.org/php-imagick-setimagetype-function/)

**Imagick：：setImageType()函数**是 PHP 中的内置函数，用于设置图像类型。
**语法：**和

```php
*bool* Imagick::setImageType( *int* $image_type )
```

**参数：**此函数接受单个参数**$image_type**，该参数包含与[IMGTYPE 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.imgtype-undefined)之一相对应的整数值。 我们也可以像*setImageType(Imagick：：IMGTYPE_GRAYSCALE)；*那样直接传递常量。
所有 IMGTYPE 常量如下：

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

**返回值：**如果成功，此函数返回 TRUE。
以下程序说明 PHP：
**程序 1：**和
中的**Imagick：：setImageType()函数**

## PHP

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Type to imagick::IMGTYPE_GRAYSCALEMATTE
$imagick->setImageType(3);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/b9e5c427c0f6c1b77833b0f107c89bb8.png)

**程序 2：**和

## PHP

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Type to imagick::IMGTYPE_BILEVEL
$imagick->setImageType(1);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/c1b34dc07737d927fa12f6bec6102669.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagetype.php](https://www.php.net/manual/en/imagick.setimagetype.php)