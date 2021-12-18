# PHP|Imagick hasNextImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-hasnextimage-function/](https://www.geeksforgeeks.org/php-imagick-hasnextimage-function/)

**Imagick：：hasNextImage()函数**是 PHP 中的一个内置函数，用于检查对象是否包含更多图像。

**语法：**

```php
*bool* Imagick::hasNextImage( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个布尔值，如果对象在正向遍历列表时有更多图像，则返回 TRUE，如果没有图像，则返回 FALSE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：hasNextImage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Checking if there is any next image
$hasNextImage = $imagick->hasNextImage();

if ($hasNextImage) {
    echo 'Yes, next image is there.';
} else {
    echo 'No, there is no next image.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add a image to imagick object
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'));

// Move the cursor to first image
$imagick->setIteratorIndex(0);

// Checking if there is any next image
$hasNextImage = $imagick->hasNextImage();

if ($hasNextImage) {
    echo 'Yes, next image is there.';
} else {
    echo 'No, there is no next image.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.hasnextimage.php](https://www.php.net/manual/en/imagick.hasnextimage.php)