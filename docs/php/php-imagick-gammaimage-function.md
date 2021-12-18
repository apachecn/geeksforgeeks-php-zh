# PHP|Imagick GammaImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-gammaimage-function/](https://www.geeksforgeeks.org/php-imagick-gammaimage-function/)

**Imagick：：GammaImage()**函数是 PHP 中的一个内置函数，用于通过提供 Gamma 校正来校正图像。 在不同设备上查看相同图像时，在屏幕上显示图像强度的方式会有感知上的差异。

**语法：**

```
*bool* Imagick::gammaImage( $gamma, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Gamma：**此参数采用 Gamma 校正量。
*   **$channel：**此参数取通道的值。 默认通道的值为 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/ab91c0dc89e9cb6d5dbd5de6b47bd880.png)

下面的程序演示了 PHP 中的**Imagick：：GammaImage()**函数：

**程序：**

```
<?php 

// require_once('path/vendor/autoload.php'); 

// Image Header
header('Content-type: image/png');

// Create Imagick Object 
$image = new Imagick('img/geeksforgeeks.png');

// Use gammaimage function
$image->gammaImage(2.2, Imagick::CHANNEL_DEFAULT);

// Display output image
echo $image;
?>
```

**输出：**
![](img/3fc2945aac1808de340b593eb063757a.png)

**引用：**[http://php.net/manual/en/imagick.gammaimage.php](http://php.net/manual/en/imagick.gammaimage.php)