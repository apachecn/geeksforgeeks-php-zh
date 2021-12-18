# PHP|Imagick coalesceImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-coalesceimages-function/](https://www.geeksforgeeks.org/php-imagick-coalesceimages-function/)

Imagick：：coalscaleImages()函数是 PHP 中的一个内置函数，用于将一组图像组合成单个图像。 它根据任何页面偏移量和处理方法合成一组图像。 动画序列 GIF、MIFF 和 MNG 通常从图像背景开始，并且每个后续图像在大小和偏移量上各不相同。

**语法：**

```
*Imagick* Imagick::coalesceImages( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时返回 Imagick 对象。

下面的程序演示了 PHP 中的 Imagick：：coalscaleImages()函数：

**程序：**此程序从一组图像生成动画 gif 图像。

```
<?php

$images = [
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-16.png",
"https://media.geeksforgeeks.org/wp-content/uploads/edgeImage.png"
];

// Loading up images in an array 
$temp = new Imagick();

foreach ($images as $image) {
    $temp->readImage($image);
    $temp->setImageDelay(100);
}

// Reading each image with a delay
// of 100 millisecond time
$temp->setImageFormat('gif');
$gif = $temp->coalesceImages();

// Composing set of all images
$gif->setImageFormat('gif');

// Setting up output format to gif
$gif->setImageIterations(0);

// Infinite iterations of gif
header("Content-Type: image/gif");

// Display the image
echo $gif->getImagesBlob();

?>
```

**输出：**
![image file](img/bf2cb880a3c2f31800968ce58034a247.png)

**引用：**[https://www.php.net/manual/en/imagick.coalesceimages.php](https://www.php.net/manual/en/imagick.coalesceimages.php)