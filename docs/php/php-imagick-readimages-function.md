# PHP|Imagick readImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-readimages-function/](https://www.geeksforgeeks.org/php-imagick-readimages-function/)

**Imagick：：readImages()函数**是 PHP 中的一个内置函数，用于从文件名数组中读取图像并将其关联到单个 Imagick 对象。

**语法：**

```
*bool* Imagick::readImages( *array* $filenames )
```

**参数：**此函数接受单个参数**$filenames**，该参数保存一个包含所有文件名的数组。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：readImages()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Array of images
$images = [
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png',
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'
];

// Read the images
$imagick->readImages($images);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d2cdeddf65779f170b39764ad552411f.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Array of images
$images = [
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png',
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'
];

// Read the images
$imagick->readImages($images);

// Moving index to 0 to check if the first image
// is also inserted.
$imagick->setIteratorIndex(0);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Array of images (from local folder). For this
// to work mentioned images should be there in the
// local folder.
$images = [
    'filename1.png',
    'filename2.png'
];

// Read the images
$imagick->readImages($images);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

```
It will show filename2.png on the screen.
```

**引用：**[https://www.php.net/manual/en/imagick.readimages.php](https://www.php.net/manual/en/imagick.readimages.php)