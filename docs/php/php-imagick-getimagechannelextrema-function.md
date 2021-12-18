# PHP|Imagick getImageChannelExtrema()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechannelextrema-function/](https://www.geeksforgeeks.org/php-imagick-getimagechannelextrema-function/)

**Imagick：：getImageChannelExtrema()函数**是 PHP 中的一个内置函数，用于获取一个或多个图像通道的极值。 极值是观察到函数的最大值或最小值的点。 它返回一个具有键“MINIMA”和“MAXIMA”的关联数组。

**语法：**

```php
*array* Imagick::getImageChannelExtrema(*int* $channel)
```

**参数：**此函数接受单个参数**$channel**，该参数指定对您的通道模式有效的通道常量。 使用按位运算符组合通道类型常量。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**如果成功，此函数返回 TRUE。

以下程序说明了 PHP 中的**Imagick：：getImageChannelExtrema()函数**：

**程序 1：**

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the extrema with CHANNEL constant as 0
// which corresponds to imagick::CHANNEL_UNDEFINED
$extrema = $imagick->getImageChannelExtrema(0);
print_r($extrema);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the extrema with CHANNEL constant as 6
// which corresponds to imagick::CHANNEL_BLUE
$extrema = $imagick->getImageChannelExtrema(6);
print_r($extrema);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagechannelextrema.php](https://www.php.net/manual/en/imagick.getimagechannelextrema.php)