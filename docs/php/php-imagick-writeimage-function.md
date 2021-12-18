# PHP|Imagick WriteImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-writeimage-function/](https://www.geeksforgeeks.org/php-imagick-writeimage-function/)

**Imagick：：WriteImage()函数**是 PHP 中的一个内置函数，用于将图像写入指定的文件名。 此函数将图像文件保存在 PHP 脚本所在的同一文件夹中。

**语法：**

```
*bool* Imagick::writeImage( *string* $filename = NULL )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。 此字段是可选的，如果未提供，请将其默认设置为空或由 Imagick：：readImage()或 Imagick：：setImageFilename()设置的文件名。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：WriteImage()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add blur to image
$imagick->blurImage(12, 1);

// Give a name to file
$imagick->setImageFilename('writeImage.png');

// Write the image
$imagick->writeImage();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add floodfillPaintImage
$imagick->floodfillPaintImage("blue", 1, "white", 1, 1, false);

// Write the image with filename as 'writeImage2.png'
$imagick->writeImage('writeImage2.png');
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.writeimage.php](https://www.php.net/manual/en/imagick.writeimage.php)