# PHP|Imagick 具有 PreviousImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-haspreviousimage-function/](https://www.geeksforgeeks.org/php-imagick-haspreviousimage-function/)

**Imagick：：hasPreviousImage()函数**是 PHP 中的一个内置函数，用于检查 Imagick 对象是否有以前的图像。 如果 Imagick 对象有多个图像，则返回 TRUE，否则返回 FALSE。
**语法：**和

```php
*bool* Imagick::hasPreviousImage( void )
```

**参数：**此函数不接受任何参数。
**返回值：**如果对象在反向遍历列表时有更多图像，则此函数返回 TRUE，否则返回 FALSE。
下面的程序说明 PHP：
**程序：**中的 Imagick：：hasPreviousImage()函数。此程序演示 hasPreviousImage()函数在具有多个图像和不具有多个图像的情况下的工作。

## PHP

```php
<?php

// String array containing path of images
$imagePaths = [
"https://www.geeksforgeeks.org/wp-content/uploads/gfg_200X200.png",
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png"
];

// Create new Imagick object
$canvas = new Imagick();

$image = new Imagick(
'https://www.geeksforgeeks.org/wp-content/uploads/gfg_200X200.png');

foreach ($imagePaths as $imagePath) {

    // Adding images in the canvas
    $canvas->readImage($imagePath);
}

// The pointer points to second image
if($canvas->hasPreviousImage()) {
    echo('$canvas has Multiple Images !!');
}

if($image->hasPreviousImage()) {

    // With a single image
    echo('$image has Multiple Images !!');
}

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
$canvas has Multiple Images !!
```

**引用：**[https://www.php.net/manual/en/imagick.haspreviousimage.php](https://www.php.net/manual/en/imagick.haspreviousimage.php)