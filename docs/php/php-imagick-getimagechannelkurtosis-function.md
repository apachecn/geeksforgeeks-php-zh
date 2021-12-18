# PHP|Imagick getImageChannelKurtosis()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechannelkurtosis-function/](https://www.geeksforgeeks.org/php-imagick-getimagechannelkurtosis-function/)

**Imagick：：getImageChannelKurtosis()函数**是 PHP 中的一个内置函数，用于获取特定通道的峰度和偏度。

**语法：**

```
*array* Imagick::getImageChannelKurtosis( *int* $channel )
```

**参数：**此函数接受单个参数**$channel**，该参数用于指定对您的通道模式有效的通道常量。 如果要应用于多个通道，可以使用按位运算符组合通道类型常量。 默认值为 Imagick：：Channel_Default。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回具有峰度和偏度成员的数组。

下面的程序说明了 PHP 中的**Imagick：：getImageChannelKurtosis()函数**：

**程序 1：**

```
<?php

// Create two new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Kurtosis and Skewness
$kurtosis = $imagick1->getImageChannelKurtosis();

print_r($kurtosis);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the Kurtosis and Skewness with CHANNEL constant as 6
// which corresponds to imagick::CHANNEL_BLUE
$kurtosis = $imagick->getImageChannelKurtosis(6);

print_r($kurtosis);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagechannelkurtosis.php](https://www.php.net/manual/en/imagick.getimagechannelkurtosis.php)