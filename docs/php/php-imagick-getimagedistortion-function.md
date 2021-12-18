# PHP|Imagick getImageDistortion()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagedistortion-function/](https://www.geeksforgeeks.org/php-imagick-getimagedistortion-function/)

**Imagick：：getImageDistortion()函数**是 PHP 中的一个内置函数，用于将图像与重建图像进行比较，并返回指定的失真度量。

**语法：**

```php
*float* Imagick::getImageDistortion(*Imagick* $reference, *int* $metric)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Reference：**它指定需要比较的 Imagick 对象。
*   **$metric：**它指定[公制类型常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.metric)之一。
    度量常量列表如下：
    *   Imagick：：METRIME_UNDEFINED(0)
    *   Imagick：：Metric_MEANABSOLUTEERROR(1)
    *   Imagick：：MEANSQUAREERROR(2)
    *   Imagick：：Metric_PEAKABSOLUTEERROR(3)
    *   Imagick：：Metric_PEAKSIGNALTONOISERATIO(4)
    *   Imagick：：Metric_ROOTMEANSQUAREDERROR(5)

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回图像上使用的失真度量。

以下程序说明了 PHP 中的**Imagick：：getImageDistortion()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the distortion with METRIC constant
// as imagick::METRIC_ROOTMEANSQUAREDERROR
$distortion = $imagick1->getImageDistortion($imagick2, 5);

echo $distortion;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0.97254902124405
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the distortion with METRIC constant
// as imagick::METRIC_PEAKSIGNALTONOISERATIO
$distortion = $imagick1->getImageDistortion($imagick2, 4);

echo $distortion;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0.020707619325613
```

**程序 3：**

```php
<?php

// Create a new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the distortion with METRIC constant
// as imagick::METRIC_ROOTMEANSQUAREDERROR
$distortion = $imagick1->getImageDistortion($imagick2, 4);

echo $distortion;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0 because both images are same.
```

**引用：**[https://www.php.net/manual/en/imagick.getimagedistortion.php](https://www.php.net/manual/en/imagick.getimagedistortion.php)