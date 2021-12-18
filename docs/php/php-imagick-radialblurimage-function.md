# PHP|Imagick RadialBlurImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-radialblurimage-function/](https://www.geeksforgeeks.org/php-imagick-radialblurimage-function/)

**Imagick：：RadialBlurImage()**函数是 PHP 中的内置函数，用于创建径向模糊图像。

**语法：**

```php
*bool* Imagick::radialBlurImage( $angle, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$angle：**此参数存储角度的值。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道是 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)
下面的程序说明了 PHP：
**程序 1：**中的**Imagick RadialBlurImage()**函数

```php
<?php 

// require_once('path/vendor/autoload.php');

// Set header content
header('Content-type: image/png');

// Create new Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use radialBlurImage function
$image->radialBlurImage(5);

// Display output image
echo $image;
?>
```

**输出：**
![](img/23633adb2a4281543e188cf427be0a5b.png)

**程序 2：**

```php
<?php 

// require_once('path/vendor/autoload.php');

// Create new Imagick Object
$imagick = new Imagick('img/geeksforgeeks.png');

// Use radialBlurImage function
$imagick->radialBlurImage(6, 10);

// Function to write image
$imagick->writeImage('radialBlurImage1.png');

// Destroy Imagick object
$imagick->destroy();
?>
```

**输出：**
![Radial Blur Image](img/ee17cbed0b8760f919a8004ab66d25d0.png)

**引用：**[http://php.net/manual/en/imagick.radialblurimage.php](http://php.net/manual/en/imagick.radialblurimage.php)