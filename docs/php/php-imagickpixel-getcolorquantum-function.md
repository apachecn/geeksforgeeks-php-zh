# PHP|ImagickPixel getColorQuantum()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getcolorquantum-function/](https://www.geeksforgeeks.org/php-imagickpixel-getcolorquantum-function/)

**ImagickPixel：：getColorQuantum()函数**是 PHP 中的一个内置函数，用于获取数组中像素的颜色作为量子值。 此函数返回一个具有键 r、g、b 的数组，每个键分别代表红色、绿色、蓝色和 Alpha/不透明度。 量子值的范围从 0 到 65535，其中 0 是最低值，65535 是最高值，即不透明度为 0 表示透明，65535 表示不透明。

**语法：**

```php
*array* ImagickPixel::getColorQuantum( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含量子值的数组。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixel：：getColorQuantum()函数**：

**程序 1：**

```php
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Get the color quantum
$colorQuantum = $imagickPixel->getColorQuantum();
print("<pre>".print_r($colorQuantum, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the color
$imagickPixel->setColor('#48c268');

// Get the color quantum
$colorQuantum = $imagickPixel->getColorQuantum();
print("<pre>".print_r($colorQuantum, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixel.getcolorquantum.php](https://www.php.net/manual/en/imagickpixel.getcolorquantum.php)