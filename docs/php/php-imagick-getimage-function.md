# PHP|Imagick getImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimage-function/](https://www.geeksforgeeks.org/php-imagick-getimage-function/)

**Imagick：：getImage()函数**是 PHP 中的一个内置函数，用于获取 Imagick 对象的当前图像序列。 此函数用于将一个 Imagick 对象的内容复制到新变量中。

**语法：**

```php
*string* Imagick::getImage( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**如果成功，此函数将返回一个新的 Imagick 对象。

下面的程序演示了 PHP 中的**Imagick：：getFilename()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$source_imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Copy the Image to another variable
$destination_imagick = $source_imagick->getImage();

// Check if image is there in new variable
header("Content-Type: image/png");

echo $destination_imagick->getImageBlob();
?>
```

**输出：**
![](img/77c36ca0c1fed4bb69d0f145636d68af.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$source_imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Add a new imagick image to next position
$source_imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190914153420/paintopaque.png'));

// Copy the Image to another variable
$destination_imagick = $source_imagick->getImage();

// Check if next image is also there
$destination_imagick->nextImage();

header("Content-Type: image/png");
echo $destination_imagick->getImageBlob();
?>
```

**输出：**
![](img/bea665d73edbe905c94223b53f290b68.png)

**引用：**[https://www.php.net/manual/en/imagick.getimage.php](https://www.php.net/manual/en/imagick.getimage.php)