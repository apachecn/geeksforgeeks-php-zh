# PHP|imagecolorsforindex()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorsforindex-function/](https://www.geeksforgeeks.org/php-imagecolorsforindex-function/)

**imagecolorsforindex()**函数是 PHP 中的一个内置函数，用于获取给定索引处的颜色。 此函数返回包含指定颜色值的红、绿、蓝和 Alpha 键值的数组。
**语法：**和

```php
*array* imagecolorsforindex ( $image, $index )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**imagecreatetruecolor()函数用于创建给定大小的图像。 此函数用于创建给定大小的空白图像。
*   **$index：**此参数用于指定颜色索引。

**返回值：**此函数返回一个关联数组，该数组包含给定索引处的红、绿、蓝和 Alpha 键值。下面的程序说明了 PHP：
**程序 1：**和
中的**imagecolorsforindex()**函数

## PHP

```php
<?php

// store the image in variable.
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Calculate rgb pixel value at particular point.
$rgb = imagecolorat($image, 30, 25);

// Assign color name and its value.
$colors = imagecolorsforindex($image, $rgb);

var_dump($colors);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
array(4) { 
    ["red"]=> int(34) 
    ["green"]=> int(170) 
    ["blue"]=> int(66) 
    ["alpha"]=> int(0) 
} 
```

**程序 2：**和

## PHP

```php
<?php

// store the image in variable.
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/col1.png');

// index value
$index_x = 230;
$index_y = 120;

// Calculate rgb pixel value at particular point.
$rgba_color = imagecolorat($image, $index_x, $index_y);

// Assign color name and its value.
$colors = imagecolorsforindex($image, $rgba_color);

var_dump($colors);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
array(4) { 
    ["red"]=> int(97) 
    ["green"]=> int(57) 
    ["blue"]=> int(104) 
    ["alpha"]=> int(0) 
} 
```

**相关文章：**和

*   [PHP|imagecolorclosestapha()函数](https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/)
*   [PHP|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)

**引用：**[http://php.net/manual/en/function.imagecolorsforindex.php](http://php.net/manual/en/function.imagecolorsforindex.php)