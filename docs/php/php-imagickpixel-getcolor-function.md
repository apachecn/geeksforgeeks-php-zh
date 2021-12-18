# PHP|ImagickPixel getColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getcolor-function/](https://www.geeksforgeeks.org/php-imagickpixel-getcolor-function/)

**ImagickPixel：：getColor()函数**是 PHP 中的一个内置函数，用于获取 ImagickPixel 对象以数组形式描述的颜色。 如果颜色设置了不透明度通道，则该值将作为列表中的第四个值提供。 数组的关键点是 r 为(红色)、b 为(蓝色)、g 为(绿色)和 a 为(Alpha/不透明度)。

**语法：**

```php
*array* ImagickPixel::getColor( *int* $normalized )
```

**参数：**此函数接受单个参数**$Normalized**，该参数指示是否规格化值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixel：：getColor()函数**：

**程序 1：**

```php
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel(); 

// Get the color
$color = $imagickPixel->getColor();

// Print the color
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagickPixel object
// with a color
$imagickPixel = new ImagickPixel('#3539bd'); 

// Get the color
$color = $imagickPixel->getColor();

// Print the color
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 3：**

```php
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel(); 

// Set the color
$imagickPixel->setColor('#38d9d3');

// Get the color
$color = $imagickPixel->getColor();

// Print the color
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixel.getcolor.php](https://www.php.net/manual/en/imagickpixel.getcolor.php)