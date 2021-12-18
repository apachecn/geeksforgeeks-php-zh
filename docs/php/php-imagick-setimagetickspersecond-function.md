# PHP|Imagick setImageTicksPerSecond()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagetickspersecond-function/](https://www.geeksforgeeks.org/php-imagick-setimagetickspersecond-function/)

**Imagick：：setImageTicksPerSecond()函数**是 PHP 中的一个内置函数，用于设置每秒的图像刻度，这意味着显示一帧动画图像的时间。

**语法：**

```php
*bool* Imagick::setImageTicksPerSecond( *int* $ticks_per_second )
```

**参数：**此函数接受单个参数**$ticks_per_Second**，该参数保存图像应显示的持续时间，以每秒刻度表示。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageTicksPerSecond()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// Set the image ticks per second
$imagickAnimation->setImageTicksPerSecond(800);

// Display the image
header("Content-Type: image/gif");
echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/d1fedf2d43cabdfa5a6d1cc3e6dbb31f.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

// Set the image ticks per second
$imagickAnimation->setImageTicksPerSecond(2000);

// Display the image
header("Content-Type: image/gif");
echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/a882fb39103a5b28522274985799e157.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagetickspersecond.php](https://www.php.net/manual/en/imagick.setimagetickspersecond.php)