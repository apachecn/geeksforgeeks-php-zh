# PHP|Imagick MosaicImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-mosaicimages-function/](https://www.geeksforgeeks.org/php-imagick-mosaicimages-function/)

**Imagick：：MosaicImages()函数**是 PHP 中的一个内置函数，用于从图像形成马赛克。 此函数使用图像序列来形成单个相干图片。

**语法：**

```php
*Imagick* Imagick::mosaicImages( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的 Imagick：：MosaicImages()函数：

**程序：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Set the width, height and background
// color of an image
$imagick->newimage(500, 200, 'green');

// Store the images in an array
$imagesArray = [
"https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png",
"https://media.geeksforgeeks.org/wp-content/uploads/20190826132815/download7.png"
];

// Set the position of each image
$positionsArray = [
    [0, 0],
    [0, 100]
];

// Adding images from set and setting image pages
for( $i = 0; $i < 2; $i++) {

    $nextImage = new Imagick($imagesArray[$i]);

    $nextImage->resizeimage(300, 300, Imagick::FILTER_LANCZOS, 1.0, true);

    $nextImage->setImagePage(
        $nextImage->getImageWidth(),
        $nextImage->getImageHeight(),
        $positionsArray[$i][0],
        $positionsArray[$i][1]
    );

    $imagick->addImage($nextImage);
}

// Use mosaicImages() function
$result = $imagick->mosaicImages();

// Set the image format
$result->setImageFormat('png');

header("Content-Type: image/png");

// Display the output image
echo $result->getImageBlob();
?>
```

**输出：**
![](img/7f6db836b796bc84f82ff9435ce91a66.png)

**引用：**[https://www.php.net/manual/en/imagick.mosaicimages.php](https://www.php.net/manual/en/imagick.mosaicimages.php)