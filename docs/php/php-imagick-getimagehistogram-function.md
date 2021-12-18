# PHP|Imagick getImageHistgraph()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagehistogram-function/](https://www.geeksforgeeks.org/php-imagick-getimagehistogram-function/)

**Imagick：：getImageHistgraph()函数**是 PHP 中的一个内置函数，用于获取图像直方图。

**语法：**

```php
*array* Imagick::getImageHistogram( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像直方图的 ImagickPixel 对象数组。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageHistgraph()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Histogram
$histogram = $imagick->getImageHistogram();

print("<pre>".print_r($histogram, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the Histogram
$histogram = $imagick->getImageHistogram();

print("<pre>".print_r($histogram, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagehistogram.php](https://www.php.net/manual/en/imagick.getimagehistogram.php)