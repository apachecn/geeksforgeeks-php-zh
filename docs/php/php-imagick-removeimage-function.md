# PHP|Imagick removeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-removeimage-function/](https://www.geeksforgeeks.org/php-imagick-removeimage-function/)

**Imagick：：removeImage()函数**是 PHP 中的一个内置函数，用于从图像列表中删除图像。 此函数用于删除光标指向的当前图像。

**语法：**

```
*bool* Imagick::removeImage( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：removeImage()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Count the image
echo 'Number of images before removing: '. $imagick->count() . '<br>';

// Remove the Image
$imagick->removeImage();

// Count the image
echo 'Number of images after removing: '. $imagick->count();;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add a new image to Imagick object
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'));

// Count the image
echo 'Number of images before removing: '. $imagick->count() . '<br>';

// Remove the Image
$imagick->removeImage();

// Count the image
echo 'Number of images after removing: '. $imagick->count();;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.removeimage.php](https://www.php.net/manual/en/imagick.removeimage.php)