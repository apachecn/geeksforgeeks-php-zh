# PHP|Imagick getImage 重力()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagegravity-function/](https://www.geeksforgeeks.org/php-imagick-getimagegravity-function/)

**Imagick：：getImage 重力()函数**是 PHP 中的一个内置函数，用于获取图像重力。 *getGravic()*和*getImageGrauity()*的区别在于前者应用于整个 Imagick 对象，而后者获取序列中当前图像的重力(如果有多个图像)。

**语法：**

```php
*int* Imagick::getImageGravity( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回表示图像重力常数的整数值。

重力常数列表如下所示：

*   Imagick：：Grasion_Northwest(0)
*   Imagick：：Grasion_North(1)
*   Imagick::Graight_ Northeast (2)
*   Imagick：：Grasion_West(3)
*   Imagick：：Graight_Center(4)
*   Imagick：：Graight_East(5)
*   Imagick：：Gragation_East(5)
*   Imagick：：Graight_West(3)
*   Imagick：：Graight_Center(4)

*   Imagick：：Grasion_South(7)
*   Imagick::Grasion_ Southeast (8)

下面的程序说明了 PHP 中的**Imagick：：getImage 重力()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Gravity
$gravity = $imagick->getImageGravity();
echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gravity
$imagick->setImageGravity(4);

// Get the Gravity
$gravity = $imagick->getImageGravity();

echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagegravity.php](https://www.php.net/manual/en/imagick.getimagegravity.php)