# PHP|Imagick patOpaqueImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-paintopaqueimage-function/](https://www.geeksforgeeks.org/php-imagick-paintopaqueimage-function/)

**Imagick：：aint tOpaqueImage()函数**是 PHP 中的一个内置函数，用于更改与特定颜色匹配的任何像素。
**语法：**

```php
*bool* Imagick::paintOpaqueImage
($target, $fill, $fuzz, $channel = Imagick::CHANNEL_DEFAULT)
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$target：**此参数保存要更改的目标颜色。
*   **$Fill：**此参数保存要更改的颜色。
*   **$fuzz：**此参数定义将两种颜色视为相同可接受的公差。
*   **$channel：**此参数保存 Imagick 通道常量，这些常量提供对通道模式有效的任何通道常量。 可以使用按位运算符组合多个通道。 默认值为 Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。
**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：aint tOpaqueImage()函数**：

**程序：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Applying the paintOpaqueImage function
$imagick->paintOpaqueImage('#FFFFFF', 'black', 1, Imagick::CHANNEL_DEFAULT);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/bea665d73edbe905c94223b53f290b68.png)
**参考：**[https://www.php.net/manual/en/imagick.paintopaqueimage.php](https://www.php.net/manual/en/imagick.paintopaqueimage.php)