# PHP|Imagick ConvolveImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-convolveimage-function/](https://www.geeksforgeeks.org/php-imagick-convolveimage-function/)

**Imagick：：ConvolveImage()**函数是 PHP 中的内置函数，用于将自定义卷积内核应用于图像。

**语法：**

```php
*bool* Imagick::convolveImage( $kernel, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$kernel：**此参数将卷积内核的值存储为数组。
*   **$channel：**此参数存储通道的值。 默认通道的值为 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f3f9ad737830ec5f484ea0965e65694b.png)

下面的程序演示了 PHP 中的**Imagick：：ConvolveImage()**函数：

**程序：**

```php
<?php

// require_once('path/vendor/autoload.php');

/*Imagick Object*/
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png');

$Matrix = [-1, -1, -1, -1, 8, -1, -1, -1, -1, ];
$image->setImageBias(1 * \Imagick::getQuantum());

/*convolveImage*/
$image->convolveImage($Matrix);

/*Image Header*/
header('Content-type: image/png');

// Display output image
echo $image;
?>
```

**输出：**
![](img/935548a0c18732481acb05d779e22990.png)

**引用：**[http://php.net/manual/en/imagick.convolveimage.php](http://php.net/manual/en/imagick.convolveimage.php)