# PHP|Imagick compareImageChannels()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-compareimagechannels-function/](https://www.geeksforgeeks.org/php-imagick-compareimagechannels-function/)

**Imagick：：compareImageChannels()函数**是 PHP 中的一个内置函数，用于返回一个或多个图像之间的差异。

**语法：**

```php
*array* Imagick::compareImageChannels( *Imagick* $image, *int* $channelType, *int* $metricType )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image:** this parameter saves the Imagick object that contains the image to be compared.
*   **$channel elType:** this parameter holds the Imagick channel constant, which provides any channel constant that is valid for your channel mode. Use bitwise operators to combine one or more channel constants. [Click here](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.channel) to get a list of channel constants.
*   **$metricType:** is a metric type constant. [Click here](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.channel-undefined) for a list of metric type constants.

**返回值：**返回 new_wand 和失真数组。

**错误/异常：**发生错误时抛出 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：compareImageChannels()函数：

**程序：**

```php

<?php

// Store the image path into variables
$imagePath1 =
"https://cdncontribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png";

$imagePath2 =
"https://www.geeksforgeeks.org/wp-content/uploads/gfg_200X200.png";

$imagePath3 =
"https://cdncontribute.geeksforgeeks.org/wp-content/uploads/negateImage.png";

// Create new Imagick object
$imagick1 = new \Imagick($imagePath1);
$imagick2 = new \Imagick($imagePath2);
$imagick3 = new \Imagick($imagePath3);

// Use compareImageChannels() function to find
// the difference between images
$diff12 = $imagick1->compareImageChannels($imagick2,
        Imagick::CHANNEL_ALL, Imagick::METRIC_MEANABSOLUTEERROR);

$diff13 = $imagick1->compareImageChannels($imagick3, 
        Imagick::CHANNEL_ALL, Imagick::METRIC_MEANABSOLUTEERROR);

// Print the difference in array
print_r($diff12);
print_r($diff13);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.compareimagechannels.php](https://www.php.net/manual/en/imagick.compareimagechannels.php)