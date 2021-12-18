# PHP|Imagick OptimizeImageLayers()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-optimizeimagelayers-function/](https://www.geeksforgeeks.org/php-imagick-optimizeimagelayers-function/)

**Imagick：：OptimizeImageLayers()函数**是 PHP 中的一个内置函数，用于删除要优化的图像的重复部分。 此函数用于比较 GIF 处理的序列中前一图像的每个图像。

**语法：**

```php
*bool* Imagick::optimizeImageLayers( *void*)
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

以下程序说明了 PHP 中的 Imagick：：OptimizeImageLayers()函数：

**程序：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Optimizing the image layers 
$imagick->optimizeImageLayers();

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/15e2334b5d7d81ba4457d0a46e21ba1c.png)

**引用：**[https://www.php.net/manual/en/imagick.optimizeimagelayers.php](https://www.php.net/manual/en/imagick.optimizeimagelayers.php)