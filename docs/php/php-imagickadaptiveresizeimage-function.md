# PHP|Imagick AdaptiveResizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagickadaptiveresizeimage-function/](https://www.geeksforgeeks.org/php-imagickadaptiveresizeimage-function/)

**Imagick：：AdaptiveResizeImage()**函数是 PHP 中的一个内置函数，它为图像提供了自适应调整图像大小的功能。 自适应调整图像大小的强度取决于图像边缘的显著减少。 此功能用于根据网站调整图像大小。 当它将图像略微缩小到一个稍小的“网页大小”时，它很有用。当全尺寸图像自适应地调整为缩略图时，“网页大小”可能看起来不太好。

**语法：**

```php
*bool* Imagick::adaptiveResizeImage ( $columns, $rows, $bestfit )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Columns：**该参数用于设置缩放图片中的列数。
*   **$ROWS：**该参数用于设置缩放图像的行数。
*   **$Best fit：**此参数用于检查图像是否适合边界框内。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

以下程序说明了 PHP 中的**Imagick：：AdaptiveResizeImage()**函数：

**原始图像：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序：**

```php
<?php

// require_once('path/to/vendor/autoload.php');

header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$image->adaptiveResizeImage(1024, 768);

echo $image;
?>
```

**输出：**
![adaptive resize image](img/8e7b4b5c03f21789525627b21096b058.png)

**引用：**[http://php.net/manual/en/imagick.adaptiveresizeimage.php](http://php.net/manual/en/imagick.adaptiveresizeimage.php)