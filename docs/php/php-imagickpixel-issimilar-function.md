# PHP|ImagickPixel isSimilar()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-issimilar-function/](https://www.geeksforgeeks.org/php-imagickpixel-issimilar-function/)

**ImagickPixel：：isSimilar()函数**是 PHP 中的一个内置函数，用于检查此 ImagickPixel 对象所描述的颜色与所提供对象的颜色之间的距离，方法是将它们的 RGB 值绘制在颜色立方体上。 如果两点之间的距离小于给定的模糊值，则颜色相似。

**语法：**

```
*bool* ImagickPixel::isSimilar( *ImagickPixel* $color, *float* $fuzz )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$color：**它指定包含要比较的颜色的像素。
*   **$fuzz：**它指定模糊值，该值指示将这些颜色视为相似的最大距离。

**返回值：**此函数返回布尔值，该值指示颜色是否相似(TRUE)或不相似(FALSE)。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：isSimilar()函数**

```
<?php
// Create a new imagickPixel object
$imagickPixel1 = new ImagickPixel('cyan');

// Create another new imagickPixel object
$imagickPixel2 = new ImagickPixel('pink');

// Check if similar or not
$isSimilar = $imagickPixel1->isSimilar($imagickPixel2, 0.1);

if($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Not Similar
```

**程序 2：**

```
<?php
// Create two new imagickPixel objects with same color
$imagickPixel1 = new ImagickPixel('orange');
$imagickPixel2 = new ImagickPixel('orange');

// Check if similar
$isSimilar = $imagickPixel1->isSimilar($imagickPixel2, 30);

if($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Similar
```

**程序 3：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the 1001th pixel
$imagickPixel1 = $histogramElements[1000];

// Get the 2001th pixel
$imagickPixel2 = $histogramElements[2000];

// Check if both pixels are similar
$isSimilar = $imagickPixel1->isSimilar($imagickPixel2, 400);

if ($isSimilar) {
    echo 'Similar';
} else {
    echo 'Not Similar';
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Not Similar
```

**引用：**[https://www.php.net/manual/en/imagickpixel.issimilar.php](https://www.php.net/manual/en/imagickpixel.issimilar.php)