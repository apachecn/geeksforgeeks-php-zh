# PHP|Imagick filter()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-filter-function/](https://www.geeksforgeeks.org/php-imagick-filter-function/)

Imagick：：Filter()函数是 PHP 中的一个内置函数，用于将自定义卷积内核应用于图像。 核、卷积矩阵或掩码是一个小矩阵。 它用于模糊、锐化、浮雕、边缘检测等等。

**语法：**

```
*bool* Imagick::filter( $ImagickKernel, $channel = Imagick::CHANNEL_UNDEFINED )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ImagickKernel：**它是用于应用于映像的一个内核或一系列链接的多个内核。
*   **$channel：**它是根据模式使用的常量。 整型，channel 的默认值为 Imagick：：Channel_Default。

**返回值：**成功应用图像滤镜时返回 TRUE。

下面的程序演示了 PHP 中的 Imagick：：Filter()函数：

**程序：**

```
<?php

// Declare an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Declare convolution matrix
$matrix = [
    [-1, 0, -1],
    [0,  5,  0],
    [-1, 0, -1],
];

$kernel = \ImagickKernel::fromMatrix($matrix);

$strength = 0.5;

// Scaling the image on kernel
$kernel->scale($strength, \Imagick::NORMALIZE_KERNEL_VALUE);

// Use addUnityKernel() function
$kernel->addUnityKernel(1 - $strength);

// Use filter() function 
$imagick->filter($kernel);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/902755e46b7388976935f3797bfe7b1e.png)

**引用：**[https://www.php.net/manual/en/imagick.filter.php](https://www.php.net/manual/en/imagick.filter.php)