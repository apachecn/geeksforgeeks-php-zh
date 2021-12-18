# PHP|ImagickPixel isPixelSimilar()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-ispixelsimilar-function/](https://www.geeksforgeeks.org/php-imagickpixel-ispixelsimilar-function/)

**ImagickPixel：：isPixelSimilar()函数**是 PHP 中的一个内置函数，用于检查此 ImagickPixel 对象所描述的颜色与所提供对象的颜色之间的距离，方法是将它们的 RGB 值绘制在颜色立方体上。 如果两点之间的距离小于给定的模糊值，则颜色相似。

**语法：**

```php
*bool* ImagickPixel::isPixelSimilar( *ImagickPixel* $color, *float* $fuzz )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$color：**它指定包含要比较的颜色的像素。
*   **$fuzz：**它指定模糊值，该值指示将这些颜色视为相似的最大距离。

**返回值：**此函数返回布尔值，该值指示颜色是否相似(TRUE)或不相似(FALSE)。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：isPixelSimilar()函数**

```php
<?php
// Create a new imagickPixel object
$imagickPixelwhite = new ImagickPixel('white');

// Create another new imagickPixel object
$imagickPixelblue = new ImagickPixel('blue');

// Check if similar or not
$isSimilar = $imagickPixelwhite->isPixelSimilar($imagickPixelblue, 0.1);

if($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
Not Similar
```

**程序 2：**

```php
<?php
// Create two new imagickPixel objects with same color
$imagickPixel1 = new ImagickPixel('green');
$imagickPixel2 = new ImagickPixel('green');

// Check if similar
$isSimilar = $imagickPixel1->isPixelSimilar($imagickPixel2, 0.01);

if($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
Similar
```

**程序 3：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the 501th pixel
$imagickPixel1 = $histogramElements[500];

// Get the 601th pixel
$imagickPixel2 = $histogramElements[600];

// Check if similar
$isSimilar = $imagickPixel1->isPixelSimilar($imagickPixel2, 0.01);

if ($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
Not Similar
```

**引用：**[https://www.php.net/manual/en/imagickpixel.ispixelsimilar.php](https://www.php.net/manual/en/imagickpixel.ispixelsimilar.php)