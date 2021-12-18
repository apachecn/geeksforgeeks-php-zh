# PHP|Imagick clipImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-clampimage-function/](https://www.geeksforgeeks.org/php-imagick-clampimage-function/)

**Imagick：：CallpImage()函数**是 PHP 中的一个内置函数，用于限制颜色范围从 0 到量子深度。 此功能对已在给定范围内的图像没有影响。

**语法：**

```
*bool* Imagick::clampImage( *int* $channel = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受单个参数**$channel**，该参数保存 Imagick 通道常量，这些常量提供对通道模式有效的任何通道常量。 可以使用按位运算符组合多个通道。 默认值为 Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：CallpImage()函数**：

**程序：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use clampImage() function
$imagick->clampImage();

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/c2587ac033717dec7b0ca4ad088c8283.png)

**引用：**[https://www.php.net/manual/en/imagick.clampimage.php](https://www.php.net/manual/en/imagick.clampimage.php)