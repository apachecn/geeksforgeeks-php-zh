# PHP|Imagick getImageBorderColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagebordercolor-function/](https://www.geeksforgeeks.org/php-imagick-getimagebordercolor-function/)

**Imagick：：getImageBorderColor()函数**是 PHP 中的一个内置函数，用于获取图像边框颜色。

**语法：**

```
*ImagickPixel* Imagick::getImageBorderColor( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回设置为图像边框颜色的 ImagickPixel。

下面的程序说明了 PHP 中的**Imagick：：getImageBorderColor()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use getImageBluePrimary() function
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
$imagick->setImageBorderColor('brown');

// Get the Border Color
$imagickPixelColor = $imagick->getImageBorderColor();

// Get the Color from ImagickPixel
$color = $imagickPixelColor->getColorAsString();

echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagebordercolor.php](https://www.php.net/manual/en/imagick.getimagebordercolor.php)