# PHP|ImagickPixel isPixelSimilarQuantum()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-ispixelsimilarquantum-function/](https://www.geeksforgeeks.org/php-imagickpixel-ispixelsimilarquantum-function/)

**ImagickPixel：：isPixelSimilarQuantum()函数**是 PHP 中的一个内置函数，用于检查两种颜色之间的距离是否小于指定的距离。 模糊值应在 0-65535 范围内。 此函数与*isPixelSimilar()*不同，因为它接受量子范围内的模糊，并实际将像素与颜色进行比较，而不是与另一个像素进行比较。

**语法：**

```php
*bool* ImagickPixel::isPixelSimilarQuantum( *string* $color, *string* $fuzz )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$color:** it specifies the color to compare.
*   **$fuzz:** it specifies a fuzzy value.

**返回值：**此函数返回一个布尔值，该值指示它是否相似(TRUE)或不相似(FALSE)。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixel：：isPixelSimilarQuantum()函数**：

**程序 1：**

```php
<?php
// Create a new imagick object
$imagickPixel = new ImagickPixel('green');

// Check if the pixel color is green
$isSimilar = $imagickPixel->isPixelSimilarQuantum('green', 10);

if ($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the 501th pixel
$imagickPixel1 = $histogramElements[500];

// Check if the pixel color is red
$isSimilar = $imagickPixel1->isPixelSimilarQuantum('red', 10);

if ($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixel.ispixelsimilarquantum.php](https://www.php.net/manual/en/imagickpixel.ispixelsimilarquantum.php)