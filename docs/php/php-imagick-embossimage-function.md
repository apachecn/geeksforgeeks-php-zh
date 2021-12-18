# PHP|Imagick EmbossImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-embossimage-function/](https://www.geeksforgeeks.org/php-imagick-embossimage-function/)

**Imagick：：embossImage()**函数是 PHP 中的一个内置函数，用于返回具有三维效果的灰度图像。 此函数将图像与给定半径和标准差的高斯运算符进行卷积。

**语法：**

```php
*bool* Imagick::embossImage( $radius, $sigma )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$RADIUS：**此参数存储效果半径的值。
*   **$sigma：**此参数存储效果的 sigma 值。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/2aee72e5320a85a6e747db7b6fa1345f.png)

下面的程序演示了 PHP 中的**Imagick：：embossImage()**函数：

**程序：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

header('Content-type: image/png');

// Create an Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-16.png');

// Use embossImage function
$image->embossImage(7, 3);

// Display output image
echo $image;
?>
```

**输出：**
![](img/4feba4ed3731165555881dec26d43b26.png)

**引用：**[http://php.net/manual/en/imagick.embossimage.php](http://php.net/manual/en/imagick.embossimage.php)