# PHP|Imagick enhanceImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-enhanceimage-function/](https://www.geeksforgeeks.org/php-imagick-enhanceimage-function/)

**Imagick：：enhanceImage()**函数是 PHP 中的一个内置函数，用于改善噪声图像的质量。 此功能应用数字滤波器来提高质量。

**语法：**

```php
*bool* Imagick::enhanceImage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/2aee72e5320a85a6e747db7b6fa1345f.png)

下面的程序演示了 PHP 中的**Imagick：：enhanceImage()**函数：

**程序：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

header('Content-type: image/png');

// Create an Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-16.png');

// Use enhanceImage function
$image->enhanceImage();

// Display the output image
echo $image;
?>
```

**输出：**
![](img/a5db75825d87fa41f1116b573785d411.png)
**参考：**[http://php.net/manual/en/imagick.enhanceimage.php](http://php.net/manual/en/imagick.enhanceimage.php)