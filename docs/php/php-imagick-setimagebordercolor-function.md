# PHP|Imagick setImageBorderColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagebordercolor-function/](https://www.geeksforgeeks.org/php-imagick-setimagebordercolor-function/)

**Imagick：：setImageBorderColor()函数**是 PHP 中的一个内置函数，用于设置图像边框颜色。

**语法：**

```
*bool* Imagick::setImageBorderColor( *mixed* $border )
```

**参数：**此函数接受保存边框颜色的单个参数**$bord**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageBorderColor()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Border Color
$imagick->setImageBorderColor('violet');

// Get the Border Color
$imagickPixelColor = $imagick->getImageBorderColor();

// Get the Color from ImagickPixel
$color = $imagickPixelColor->getColorAsString();

echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Border Color
$imagick->setImageBorderColor('pink');

// Get the Border Color
$imagickPixelColor = $imagick->getImageBorderColor();

// Get the Color from ImagickPixel
$color = $imagickPixelColor->getColorAsString();

echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimagebordercolor.php](https://www.php.net/manual/en/imagick.setimagebordercolor.php)