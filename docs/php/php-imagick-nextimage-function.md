# PHP|Imagick nextImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-nextimage-function/](https://www.geeksforgeeks.org/php-imagick-nextimage-function/)

**Imagick：：nextImage()函数**是 PHP 中的一个内置函数，用于移动到 Imagick 实例中的下一个图像。 Imagick 实例可以由其中的图像列表组成，Imagick nextImage()将图像列表中的下一个图像与 Imagick 实例相关联。

**语法：**

```
*bool* Imagick::nextImage( void ) 
```

**参数：**此函数不接受任何参数。

**返回值：**执行成功返回 TRUE。

下面的程序演示了 PHP 中的 Imagick：：nextImage()函数：

**程序：**

```
<?php

// Declare a list of images
$images = [
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png",
"http://contribute.geeksforgeeks.org/wp-content/uploads/geek.png"
];

// List the two images to be loaded in Imagick object
$count = 0;

$image = new Imagick($images);

while($image->nextImage()) {

    // Increment count till we have next image on the list
    $count++;
}

$count++;

echo("The count of images in Imagick instance is " . $count);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.nextimage.php](https://www.php.net/manual/en/imagick.nextimage.php)