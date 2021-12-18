# PHP|Imagick setResolution()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setresolution-function/](https://www.geeksforgeeks.org/php-imagick-setresolution-function/)

**Imagick：：setResolution()函数**是 PHP 中的内置函数，用于设置图像的分辨率。 此函数不会更改图像的实际分辨率，只是在读取或创建图像之前在 Imagick 对象中设置它，要更改图像分辨率，请使用[setImageResolution()](https://www.geeksforgeeks.org/php-imagick-setimageresolution-function/)函数。 在读取或创建图像之前需要调用此函数。

**语法：**

```php
*bool* Imagick::setResolution( *float* $x_resolution, *float* $y_resolution )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x_RESOLUTION：**它指定水平分辨率。
*   **$y_Resolution：**它指定垂直分辨率。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setResolution()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the resolution
$imagick->setResolution(18, 13);

// Create new image
$imagick->newimage(100, 100, 'none');   

// Read the properties of image
print("<pre>".print_r($imagick->identifyImage(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

> 数组
> (
> [图像名称]=>
> [mimetype]=>图像/x-
> [单位]=>未定义
> [类型]=>双层
> [色彩空间]=>sRGB
> [压缩]=>未定义
> [文件大小]=>0B
> [几何图形]=[。
> [宽度]=>100
> [高度]=>100
> )
> //这里可以看到临时分辨率
> [分辨率]=>数组
> (
> [x]=>18
> [y]=>13
> )
> 
> [签名]=>e7e2dcff542de95352682dc186432e98f0188084896773f1973276b0577d5305
> )

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the resolution
$imagick->setResolution(10, 10);

// Read the image
$imagick->readimage(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Read the properties of image
print("<pre>".print_r($imagick->identifyImage(), true)."</pre>");
?>
```

> **输出：**
> Array
> (
> [ImageName]=>
> [mimetype]=>image/PNG
> [Format]=>PNG(便携网络图形)
> [单位]=>PixelsPercentieter
> [type]=>TrueColorAlpha
> [Colorspace]=[。 ][文件大小]=>45.4KB
> [几何]=>数组
> (
> [宽度]=>667
> [高度]=>184
> )
> //此处由于读取了新图像
> [分辨率]=>数组
> (
> [x]=>37.8
> [y]。 =>37.8
> )
> 
> [签名]=>f64054f5bcb4cfb82c6126eff6d3d4e6be7d0e72d5620033442cecb4b9feabbd
> )

**引用：**[https://www.php.net/manual/en/imagick.setresolution.php](https://www.php.net/manual/en/imagick.setresolution.php)