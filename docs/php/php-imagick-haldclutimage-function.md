# PHP|Imagick haldClutImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-haldclutimage-function/](https://www.geeksforgeeks.org/php-imagick-haldclutimage-function/)

**Imagick：：haldClutImage()**函数是 PHP 中的一个内置函数，用于使用 Hald 查找表替换图像中的颜色。 可以使用 Hald 颜色编码器创建 Hald 图像。

**语法：**

```php
*bool* Imagick::haldClutImage( $clut, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Clut：**此参数用于保存包含 Hald 查找图像的 Imagick 对象的值。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道是 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

下面的程序演示了 PHP 中的**Imagick：：haldClutImage()**函数：

**程序 1：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

// Create new Imagick Objects
$imagick = new \Imagick(realpath('img/geeksforgeeks.png'));
$imagickPalette = new \Imagick(realpath("img/geeksforgeeks.png"));

// Use sepiatoneImage and haldClutImage function
$imagickPalette->sepiatoneImage(50);
$imagick->haldClutImage($imagickPalette);

// Image Header
header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/9ea762ff8fa001a3afe837f585929de2.png)

**程序 2：**

```php
<?php 

// require_once('path/vendor/autoload.php');

// Create new Imagick Object
$imagick = new Imagick('img/geeksforgeeks.png');
$imagickPalette = new Imagick("img/geeksforgeeks.png");

// Use haldClutImage function
$imagickPalette->sepiatoneImage(150);
$imagick->haldClutImage($imagickPalette);

// Write output Image
$imagick->writeImage('raiseImae1.png');

// Destroy Imagick object
$imagick->destroy();
?>
```

**输出：**
![haldClutImage](img/2cb1d6ba8a544cf948a3c0387397728d.png)

**引用：**[http://php.net/manual/en/imagick.haldclutimage.php](http://php.net/manual/en/imagick.haldclutimage.php)