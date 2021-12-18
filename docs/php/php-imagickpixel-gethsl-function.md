# PHP|ImagickPixel getHSL()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-gethsl-function/](https://www.geeksforgeeks.org/php-imagickpixel-gethsl-function/)

**ImagickPixel：：getHSL()函数**是 PHP 中的一个内置函数，用于获取 ImagickPixel 对象描述的规格化 HSL 颜色，每个对象都是 0 到 1 之间的浮点数。HSL 代表色调、饱和度和亮度。 一般来说，色调决定像素的颜色，而饱和度决定颜色的强度，而亮度决定颜色是暗淡的还是明亮的。

**语法：**

```php
*array* ImagickPixel::getHSL( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 HSL 值的数组值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：getHSL()函数**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel('#d4a62a');

// Get the HSL
$hsl = $imagickPixel->getHSL();
print("<pre>".print_r($hsl, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [hue] => 0.12156862745098
    [saturation] => 0.66929133858268
    [luminosity] => 0.49803921568627
)
```

**程序 2：**

```php
<?php
// Create a new imagickPixel object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the image histogram
$histogramElements = $imagick->getImageHistogram();

// Get the 300th pixel
$getPixel = $histogramElements[300];

// Get the HSL
$hsl = $getPixel->getHSL();

print("<pre>".print_r($hsl, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [hue] => 0.54583333333333
    [saturation] => 0.29850746268657
    [luminosity] => 0.26274509803922
)
```

**引用：**[https://www.php.net/manual/en/imagickpixel.gethsl.php](https://www.php.net/manual/en/imagickpixel.gethsl.php)