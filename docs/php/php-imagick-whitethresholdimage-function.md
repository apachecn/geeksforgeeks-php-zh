# PHP|Imagick WhiteThresholdImage 函数

> Original: [https://www.geeksforgeeks.org/php-imagick-whitethresholdimage-function/](https://www.geeksforgeeks.org/php-imagick-whitethresholdimage-function/)

**Imagick：：WhiteThresholdImage()**函数是 PHP 中的一个内置函数，用于将阈值以上的所有像素转换为白色。 此函数强制阈值以上的所有像素变为白色，同时保持阈值以下的所有像素不变。

**语法：**

```
*bool* Imagick::whiteThresholdImage( $threshold )
```

**参数：**此函数接受单个参数*$Threshold*，该参数用于定义像素值的变化。

**返回值：**成功时此函数返回 True。

下面的程序说明了 PHP 中的**Imagick：：WhiteThresholdImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use whiteThresholdImage function
$imagick->whiteThresholdImage('red');

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/6d13961062ddf388ba750763439b5fc4.png)

**相关文章：**

*   [PHP|Imagick VignetteImage()函数](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)
*   [PHP|Imagick shadeImage()函数](https://www.geeksforgeeks.org/php-imagick-shadeimage-function/)

**引用：**[http://php.net/manual/en/imagick.whitethresholdimage.php](http://php.net/manual/en/imagick.whitethresholdimage.php)