# PHP|Imagick getNumberImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getnumberimages-function/](https://www.geeksforgeeks.org/php-imagick-getnumberimages-function/)

**Imagick：：getNumberImages()函数**是 PHP 中的一个内置函数，用于获取 Imagick 对象中的图像数量。 此函数还可用于计算 GIF 动画中的帧数。

**语法：**

```php
*int* Imagick::getNumberImages( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像数量的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getNumberImages()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object with a animation of 2 images
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// Get the number of Images
$number = $imagickAnimation->getNumberImages();
echo $number;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Add two more images in the same imagick object 
$imagick->addImage( new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png')); 

$imagick->addImage( new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png')); 

// Get the number of images
$number = $imagick->getNumberImages();
echo $number;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getnumberimages.php](https://www.php.net/manual/en/imagick.getnumberimages.php)