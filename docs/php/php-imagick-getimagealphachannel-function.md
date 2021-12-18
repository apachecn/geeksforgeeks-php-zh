# PHP|Imagick getImageAlphaChannel()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagealphachannel-function/](https://www.geeksforgeeks.org/php-imagick-getimagealphachannel-function/)

**Imagick：：getImageAphaChannel()函数**是 PHP 中的一个内置函数，用于获取图像 Alpha 通道。 返回值是[ALPHACHANNEL 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.alphachannel)之一。

**语法：**

```php
*int* Imagick::getImageAlphaChannel( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**成功时此函数返回整数值。

ALPHACHANNEL 常量列表如下：

*   Imagick：：ALPHACCHANNEL_ACTIVATE(0)
*   Imagick：：ALPHACCHANNEL_DEACTIVE(1)
*   Imagick：：ALPHACCHANNEL_RESET(2)
*   Imagick：：ALPHACCHANNEL_SET(3)
*   Imagick：：Alphacchannel_Extract(6)
*   Imagick：：ALPHACCHANNEL_OPAQUE(7)
*   Imagick：：ALPHACCHANNEL_SHAPE(8)
*   Imagick：：Alphacchannel_TRANSPECTION(9)

下面的程序说明了 PHP 中的**Imagick：：getImageAlphaChannel()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object with a PNG image
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Alpha Channel
$alphaChannel = $imagick->getImageAlphaChannel();

echo $alphaChannel;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object with a PNG image
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191112214917/geeksforgeeks8.jpg');

// Get the Alpha Channel
$alphaChannel = $imagick->getImageAlphaChannel();

echo $alphaChannel . "<br>";

// Set the alpha channel
$alphaChannel = $imagick->setImageAlphaChannel(imagick::ALPHACHANNEL_RESET );
// Get the Alpha Channel
$alphaChannel = $imagick->getImageAlphaChannel();

echo $alphaChannel;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagealphachannel.php](https://www.php.net/manual/en/imagick.getimagealphachannel.php)