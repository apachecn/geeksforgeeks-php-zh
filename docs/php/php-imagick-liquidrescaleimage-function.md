# PHP|Imagick iquidRescaleImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-liquidrescaleimage-function/](https://www.geeksforgeeks.org/php-imagick-liquidrescaleimage-function/)

**Imagick：：iquidRescaleImage()函数**是 PHP 中的一个内置函数，用于为一个或多个图像设置动画。 此功能主要是对图像进行重新缩放。 此函数使用液体重新缩放方法缩放图像，该方法实现了一种称为接缝雕刻的技术。
**语法：**

```
*bool* Imagick::liquidRescaleImage( $width, $height, $delta_x, $rigidity )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width：**此参数保存目标图像的宽度。
*   **$Height：**此参数保存目标图像的高度。
*   **$Delta_x：**它定义在 x 轴上穿过多少接缝。 值 0 表示直接缝。
*   **$刚性：**用于倾斜非直缝。 此参数通常为 0。

**返回值：**此函数成功时返回 True，失败时返回 False。
下面的程序说明了 PHP：
**程序：**中的 Imagick：：iquidRescaleImage()函数

## PHP

```
<?php

// Declare an Imagick object
$imagick = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190809013546/gfg_350X350.png');

// Use Imagick::liquidRescaleImage() function
$imagick->liquidRescaleImage( 500, 200, 3, 25 );

header( 'Content-Type: image/jpg' );

// Display the output
echo $imagick->getImageBlob();

?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/fc489ab04e6479f414e93860c8125e10.png)

**引用：**[https://www.php.net/manual/en/imagick.liquidrescaleimage.php](https://www.php.net/manual/en/imagick.liquidrescaleimage.php)