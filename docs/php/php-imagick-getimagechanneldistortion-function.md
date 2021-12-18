# PHP|Imagick getImageChannelDistortion()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechanneldistortion-function/](https://www.geeksforgeeks.org/php-imagick-getimagechanneldistortion-function/)

**Imagick：：getImageChannelDistortion()函数**是 PHP 中的内置函数，用于将图像的图像通道与重建图像进行比较，并返回指定的失真度量。

**语法：**

```
*float* Imagick::getImageChannelDistortion( *Imagick* $reference,
                                  *int* $channel, *int* $metric )
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **reference:** it specifies the Imagick object to compare to.
*   **channel:** it specifies the channel constant that is valid for your channel mode. To apply multiple channels, use the bitwise operator to combine channel type constants.
*   **indicator:** it specifies an indicator type constant. The list of measurement constants is as follows:
    *   Imagick：：Metric_Unfined(整数)
    *   Imagick：：MEANABSOLUTEERROR
    *   发帖主题：Re：Колибри0.7.0
    *   Imagick：：Metric_PEAKABSOLUTEERROR
    *   Imagick：：Metric_PEAKABSOLUTEERROR
    *   Imagick：：Metric_PEAKABSOLUTEERROR
    *   Imagick：

**异常：**此函数在出错时引发 ImagickException。

**返回值：**如果成功，此函数返回 TRUE。

以下程序说明了 PHP 中的**Imagick：：getImageChannelDistortion()函数**：

**程序 1：**

```
<?php

// Create two new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191112223241/trans9.png');

// Get the distortion with METRIC constant as imagick::METRIC_MEANABSOLUTEERROR
$distortion = $imagick1->getImageChannelDistortion($imagick2, 0, 1);
echo $distortion;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create two new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Get the distortion with METRIC constant
// as imagick::METRIC_MEANABSOLUTEERROR
$distortion = $imagick1->getImageChannelDistortion($imagick2, 0, 1);
echo $distortion;
?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：在第二个示例中，**输出为 0，因为两个图像相同。

**引用：**[https://www.php.net/manual/en/imagick.getimagechanneldistortion.php](https://www.php.net/manual/en/imagick.getimagechanneldistortion.php)