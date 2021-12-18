# PHP|Gmagick getimageextrema()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageextrema-function/](https://www.geeksforgeeks.org/php-gmagick-getimageextrema-function/)

**gmagick：：getimageextrema()函数**是 PHP 中的一个内置函数，用于获取图像的极值。 极值是观察到函数的最大值或最小值的点。

**语法：**

```php
*array* Gmagick::getimageextrema( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含键“min”和“max”的关联数组。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageextrema()函数**：

**程序 1(多色图像)：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the extrema
$extrema = $gmagick->getimageextrema();
print("<pre>".print_r($extrema, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(单色图像)：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/20200106200505/singlecolor.png
$gmagick = new Gmagick('singlecolor.png');

// Get the extrema
$extrema = $gmagick->getimageextrema();
print("<pre>".print_r($extrema, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimageextrema.php](https://www.php.net/manual/en/gmagick.getimageextrema.php)