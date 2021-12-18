# PHP|Imagick getImageChannelStatistics()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechannelstatistics-function/](https://www.geeksforgeeks.org/php-imagick-getimagechannelstatistics-function/)

**Imagick：：getImageChannelStatistics()函数**是 PHP 中的一个内置函数，用于获取图像中每个通道的统计信息。

**语法：**

```
*array* Imagick::getImageChannelStatistics( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回一个以统计数据作为数组成员的数组。

下面的程序说明了 PHP 中的**Imagick：：getImageChannelStatistics()函数**：

**程序 1：**

```
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the statistics
$statistics = $imagick->getImageChannelStatistics();
print("<pre>".print_r($statistics, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the statistics
$statistics = $imagick->getImageChannelStatistics();
print("<pre>".print_r($statistics, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagechannelstatistics.php](https://www.php.net/manual/en/imagick.getimagechannelstatistics.php)