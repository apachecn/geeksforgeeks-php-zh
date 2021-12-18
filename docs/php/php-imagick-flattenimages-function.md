# PHP|Imagick FltenImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-flattenimages-function/](https://www.geeksforgeeks.org/php-imagick-flattenimages-function/)

**Imagick：：FltenImages()**函数是 PHP 中的一个内置函数，用于合并图像序列。 这对于将 Photoshop 图层合并到单个图像中非常有用。

**语法：**

```php
*Imagick* Imagick::flattenImages( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/ab91c0dc89e9cb6d5dbd5de6b47bd880.png)

下面的程序演示了 PHP 中的**Imagick：：FltenImages()**函数：

**程序：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

/*Image Header*/
header('Content-type: image/png');

/*Imagick Object */
$image = new Imagick('img/geeksforgeeks.png');

/*flattenimages*/
$image->flattenimages();

// Display output image
echo $image;
?>
```

**输出：**
![](img/8b828eeb7189b43658d90533e58fb454.png)

**引用：**[http://php.net/manual/en/imagick.flattenimages.php](http://php.net/manual/en/imagick.flattenimages.php)