# PHP|Imagick setImageInterlaceScheme()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageinterlacescheme-function/](https://www.geeksforgeeks.org/php-imagick-setimageinterlacescheme-function/)

**Imagick：：setImageInterlaceScheme()函数**是 PHP 中的一个内置函数，用于设置图像的隔行扫描方案。
**语法：**和

```
*bool* Imagick::setImageInterlaceScheme( *int* $interlace_scheme )
```

**参数：**此函数接受与[隔行扫描常数](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.interlace-undefined)之一相对应的单个参数**$interlace_scheme**。 您也可以直接传递常量，如
*$Imagick->setImageInterlaceScheme(imagick：：INTERLACE_LINE)；*。
隔行扫描常量列表如下：

*   Imagick：：Interlace_ 未定义(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Interlace_Plane(3)
*   Imagick：：Interlace_Partition(4)
*   Imagick：：Interlace_GIF(5)
*   Imagick：：Interlace_JPEG(6)
*   Imagick：：interlace_png(7)

**返回值：**如果成功，此函数返回 TRUE。
**异常：**此函数在出错时引发 ImagickException。
下面的程序说明 PHP：
**程序 1：**和
中的**Imagick：：setImageInterlaceScheme()函数**

## PHP

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interlace Scheme
$imagick->setImageInterlaceScheme(imagick::INTERLACE_JPEG);

// Display the image
echo $imagick->getImageInterlaceScheme();
?>
```

发帖主题：Re：Колибри0.7.8.0

```
6
```

**程序 2：**和

## PHP

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interlace Scheme
$imagick->setImageInterlaceScheme(imagick::INTERLACE_PARTITION);

// Display the image
echo $imagick->getImageInterlaceScheme();
?>
```

发帖主题：Re：Колибри0.7.8.0

```
4
```

**引用：**[https://www.php.net/manual/en/imagick.setimageinterlacescheme.php](https://www.php.net/manual/en/imagick.setimageinterlacescheme.php)