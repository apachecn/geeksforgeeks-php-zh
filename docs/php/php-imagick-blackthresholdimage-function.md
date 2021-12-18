# PHP|Imagick BlackThresholdImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-blackthresholdimage-function/](https://www.geeksforgeeks.org/php-imagick-blackthresholdimage-function/)

**Imagick：：BlackThresholdImage()**函数是 PHP 中的一个内置函数，它强制阈值以下的所有像素变为黑色，而保持阈值以上的所有像素不变。

**语法：**

```php
*bool* Imagick::blackThresholdImage( $threshold )
```

**参数：**此函数接受单个参数*$Threshold*，该参数是必需的。 所有低于阈值的像素值，所有内容都变为黑色。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：BlackThresholdImage()**函数：

**程序：**

```php
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use blackthresholdimage function
$imagick->blackthresholdimage('rgb(127, 127, 127)');

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/b22e741f8e76a17739a3c4b35b2d9e7e.png)

**相关文章：**

*   [PHP|Imagick transverseImage()函数](https://www.geeksforgeeks.org/php-imagick-transverseimage-function/)
*   [PHP|Imagick VignetteImage()函数](https://www.geeksforgeeks.org/php-imagick-vignetteimage-function/)

**引用：**[http://php.net/manual/en/imagick.blackthresholdimage.php](http://php.net/manual/en/imagick.blackthresholdimage.php)