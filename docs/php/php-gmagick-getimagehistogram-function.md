# PHP|Gmagick getimagecolumn()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagehistogram-function/](https://www.geeksforgeeks.org/php-gmagick-getimagehistogram-function/)

**gmagick：：getimagestangraph()函数**是 PHP 中的一个内置函数，用于获取图像直方图。 此函数以 Gmagick 像素数组的形式返回图片中的所有像素。 我们可以使用此函数逐个像素地分析任何图片的颜色。

**语法：**

```php
*array* Gmagick::getimagehistogram( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含直方图的数组值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagehistgraph()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the histogram
$histogram = $gmagick->getimagehistogram();
print("<pre>".print_r($histogram, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the histogram
$histogram = $gmagick->getimagehistogram();

echo "Color of first five pixels are <br>";
for ($i = 0; $i < 5; $i++) {
    // Get the color of ith pixel
    $color = $histogram[$i]->getcolor();
    echo $color . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagehistogram.php](https://www.php.net/manual/en/gmagick.getimagehistogram.php)