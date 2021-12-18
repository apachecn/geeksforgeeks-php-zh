# PHP|Gmagick getimagegamma()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagegamma-function/](https://www.geeksforgeeks.org/php-gmagick-getimagegamma-function/)

**gmagick：：getimagegamma()函数**是 PHP 中的一个内置函数，用于获取图像 Gamma。 伽马是一种非线性运算，用于编码和解码图像中的亮度或三刺激值。

**语法：**

```
*float* Gmagick::getimagegamma( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含伽马的浮点值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagegamma()函数**：

**程序 1(多色图像)：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the gamma
$gamma = $gmagick->getimagegamma();
echo $gamma;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(单色图像)：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/20200106200505/singlecolor.png
$gmagick = new Gmagick('singlecolor.png');

// Get the gamma
$gamma = $gmagick->getimagegamma();
echo $gamma;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagegamma.php](https://www.php.net/manual/en/gmagick.getimagegamma.php)