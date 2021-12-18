# PHP|Imagick getImageChannelMean()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechannelmean-function/](https://www.geeksforgeeks.org/php-imagick-getimagechannelmean-function/)

**Imagick：：getImageChannelMean()函数**是 PHP 中的内置函数，用于获取一个或多个图像通道的平均值和标准差。 它返回一个关联数组，该数组包含键作为“Mean”，值作为“StandardDeumation”。

**语法：**

```php
*array* Imagick::getImageChannelMean(*int* $channel)
```

**参数：**此函数接受单个参数**$channel**，该参数保存对您的通道模式有效的通道常量。 使用按位运算符合并多个通道类型常量。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：getImageChannelMean()函数**：

**程序 1：**

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the mean with CHANNEL constant as 1
// which corresponds to imagick::CHANNEL_RED
$mean = $imagick->getImageChannelMean(1);

print_r($mean);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the mean with CHANNEL constant as 5
// which corresponds to imagick::CHANNEL_MAGENTA
$mean = $imagick->getImageChannelMean(5);

print_r($mean);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagechannelmean.php](https://www.php.net/manual/en/imagick.getimagechannelmean.php)