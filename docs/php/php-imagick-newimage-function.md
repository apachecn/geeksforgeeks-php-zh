# PHP|Imagick newimage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-newimage-function/](https://www.geeksforgeeks.org/php-imagick-newimage-function/)

**Imagick：：newImage()**函数是 PHP 中的内置函数，用于创建新图像。 此函数用于创建新图像并将 ImagickPixel 值关联为背景颜色。

**语法：**

```php
*bool* Imagick::newImage( $cols, $rows, $background, $format )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$cols：**该参数用于设置镜像的列。
*   **$ROWS：**此参数用于设置图像行。
*   **$BACKGROUND：**该参数用于设置图片的背景颜色。
*   **$format：**此参数用于定义图像格式。

**返回值：**成功时此函数返回 True。
**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：newImage()**函数：

**程序：**

## PHP

```php
<?php

// Create an Imagick object
$image = new Imagick();

// Use newImage function to create new image
$image->newImage(650, 400, new ImagickPixel('green'));

// Set the image format
$image->setImageFormat('png');

header('Content-type: image/png');

// Display the output image
echo $image;
?>
```

发帖主题：Re：Колибри0.7.0

![](img/a2e9d32ae541af7ed2f8b65158d7e455.png)

**引用：**[http://php.net/manual/en/imagick.newimage.php](http://php.net/manual/en/imagick.newimage.php)