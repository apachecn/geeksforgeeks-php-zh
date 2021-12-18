# PHP|Imagick solarizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-solarizeimage-function/](https://www.geeksforgeeks.org/php-imagick-solarizeimage-function/)

**Imagick：：solarizeImage()**函数是 PHP 中的内置函数，用于将日光效果应用于图像。 在照相暗室中，通过选择性地将感光纸区域暴露在光线下而获得的图像效果。

**语法：**

```
*bool* Imagick::solarizeImage( $threshold )
```

**参数：**此函数接受单个参数*$Threshold*，该参数用于测量日晒程度。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：solarizeImage()**函数：

**程序：**

```
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use solarizeImage image
$imagick->solarizeImage(0.2);

header("Content-Type: image/jpg");

// display the image content
echo $imagick->getImageBlob();
?>
```

**输出：**
![solerized image](img/b81efc2595be70367dd9edccbe3a16a7.png)

**相关文章：**

*   [PHP|Imagick shadeImage()函数](https://www.geeksforgeeks.org/php-imagick-shadeimage-function/)
*   [PHP|Imagick getImageGamma()函数](https://www.geeksforgeeks.org/php-imagick-getimagegamma-function/)

**引用：**[http://php.net/manual/en/imagick.solarizeimage.php](http://php.net/manual/en/imagick.solarizeimage.php)