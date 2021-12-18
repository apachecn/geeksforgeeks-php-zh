# PHP|Imagick getPointSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getpointsize-function/](https://www.geeksforgeeks.org/php-imagick-getpointsize-function/)

**Imagick：：getPointSize()函数**是 PHP 中的一个内置函数，用于获取 Imagick 对象的磅大小。

**语法：**

```
*float* Imagick::getPointSize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个包含点大小的浮点值。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getPointSize()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get point size
$pointSize = $imagick->getPointSize();

echo $pointSize;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set point size
$imagick->setPointSize(5);

// Get point size
$pointSize = $imagick->getPointSize();
echo $pointSize;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getpointsize.php](https://www.php.net/manual/en/imagick.getpointsize.php)