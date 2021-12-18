# PHP|Imagick ThumbnailImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-thumbnailimage-function/](https://www.geeksforgeeks.org/php-imagick-thumbnailimage-function/)

**Imagick：：ThumbnailImage()**函数是 PHP 中的一个内置函数，用于将图像的大小更改为给定的尺寸，并删除任何关联的配置文件。 此功能的目标是生成适合在 Web 上显示的小的、低成本的缩略图。

**语法：**

```
*bool* Imagick::thumbnailImage( $columns, $rows, $bestfit, $fill, 
$legacy )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$Columns：**此参数用于设置图像宽度。
*   **$row：**此参数用于设置图像高度。
*   **Best Fit：**此参数描述是否强制使用最大值。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：ThumbnailImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Function to set the background color
$imagick->setbackgroundcolor('rgb(64, 64, 64)');

// Use thumbnailImage function
$imagick->thumbnailImage(100, 100, true, true);
header("Content-Type: image/jpg");

// Display the output image    
echo $imagick->getImageBlob();
?>
```

**输出：**
![thumbnail image](img/67b2cc5a34445d618d552ba9e720d5f9.png)

**相关文章：**

*   [PHP|Imagick AdaptiveBlurImage()函数](https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/)
*   [PHP|Imagick brightnessContrastImage()函数](https://www.geeksforgeeks.org/php-imagick-brightnesscontrastimage-function/)

**引用：**[http://php.net/manual/en/imagick.thumbnailimage.php](http://php.net/manual/en/imagick.thumbnailimage.php)