# PHP|ImagickPixel getColorCount()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getcolorcount-function/](https://www.geeksforgeeks.org/php-imagickpixel-getcolorcount-function/)

**ImagickPixel：：getColorCount()函数**是 PHP 中的一个内置函数，用于获取与像素颜色相关联的颜色计数。 颜色计数是图像中与此 ImagickPixel 具有相同颜色的像素数。 *getColorCount()*似乎只适用于通过*getImageHistgraph()*创建的 ImagickPixel 对象。

**语法：**

```
*int* ImagickPixel::getColorCount( *void* ) : int
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含颜色计数的整数。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：getColorCount()函数**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the last index
$lastIndex = count($histogramElements) - 1;

// Get the element from array which is 
// a ImagickPixel object
$lastColor = $histogramElements[$lastIndex];

// Get the Color count
echo $lastColor->getColorCount();
?>
```

发帖主题：Re：Колибри0.7.0

```
18
```

**程序 2：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the element from array which is 
// a ImagickPixel object
$lastColor = $histogramElements[0];

// Get the Color count
echo $lastColor->getColorCount();
?>
```

发帖主题：Re：Колибри0.7.0

```
1
```

**程序 3：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the element from array which is 
// a ImagickPixel object
$firstColor = $histogramElements[0];

// Set the Color count
$firstColor->setColorCount(20);

// Get the Color count
echo $firstColor->getColorCount();
?>
```

发帖主题：Re：Колибри0.7.0

```
20
```

**程序 3：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the whole color stats
echo "R G B Hue :Count<br>";
foreach ($histogramElements as $pixel) {
    $colors = $pixel->getColor();
    foreach ($colors as $color) {
        print($color . " ");
    }
    print(":" . $pixel->getColorCount() . "<br>");
}
?>
```

发帖主题：Re：Колибри0.7.0

```
R G B Hue :Count
0 22 35 1 :1
0 25 37 1 :1
0 24 37 1 :1
0 31 43 1 :1
0 32 44 1 :1
0 33 45 1 :1
0 37 49 1 :3
.
.
.
```

**引用：**[https://www.php.net/manual/en/imagickpixel.getcolorcount.php](https://www.php.net/manual/en/imagickpixel.getcolorcount.php)