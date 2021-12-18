# PHP|Imagick Morimages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-morphimages-function/](https://www.geeksforgeeks.org/php-imagick-morphimages-function/)

**Imagick：：MorimImages**函数是 PHP 中的一个内置函数，用于变形一组图像。 图像像素和图像大小被线性插值，以给出从一幅图像到下一幅图像的变形外观。

**语法：**

```php
*Imagick* Imagick::morphImages( $number_frames )
```

**参数：**此函数接受单个参数*$number_frame*，该参数用于存储要生成的中间图像的数量。

**返回值：**此函数成功时返回新的 Imagick 对象。

**原图：**

![](img/88de27cfd5946382de41bc08b810f991.png)![](img/8c7c0b41a02ca0cdc660d21ce252a040.png)![](img/71ac50257e9a2f202d8078667c4a2a51.png)
![](img/d90dce7e32a82ffb1c7af60f3e3a17cd.png)
![](img/5f7032c8f0f923af4be926dabea864cf.png)

下面的程序演示了 PHP 中的**Imagick：：morImages**函数：

**程序：**

## PHP

```php
<?php

// Set of images
$images = [
    "img/geeksforgeeks.png",
    "img/charcoalImage.png",
    "img/colorMatrix.png",
    "img/adaptiveThresholdImage.png",
    "img/recolorImage.png",
];

// Create new Imagick object
$imagick = new \Imagick(realpath($images[count($images) - 1]));

foreach ($images as $image) {
    $nextImage = new \Imagick(realpath($image));
    $imagick->addImage($nextImage);
}

$imagick->resetIterator();

// Use morphImages function
$morphed = $imagick->morphImages(5);
$morphed->setImageTicksPerSecond(10);

header("Content-Type: image/gif");

// Set the image format
$morphed->setImageFormat('gif');

// Display the output image
echo $morphed->getImagesBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/9d46b1709e08abfb509433e8a2006d25.png)

**引用：**[http://php.net/manual/en/imagick.morphimages.php](http://php.net/manual/en/imagick.morphimages.php)