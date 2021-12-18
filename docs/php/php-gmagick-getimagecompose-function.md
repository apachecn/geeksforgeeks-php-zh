# PHP|Gmagick getimageccompose()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagecompose-function/](https://www.geeksforgeeks.org/php-gmagick-getimagecompose-function/)

**gmagick：：getimageccompose()函数**是 PHP 中的一个内置函数，用于获取与图像相关联的复合运算符。 合成运算符决定用于图像合成的方法。 复合运算符可以是给定的[复合运算符常数](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.composite-default)中的任何一个。

**语法：**

```
*int* Gmagick::getimagecompose( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 Compose 运算符的整数值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageccompose()函数**：

**程序 1：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image compose
$compose =  $gmagick->getimagecompose();
echo $compose;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image compose
$gmagick->setimagecompose(Gmagick::COMPOSITE_COLORIZE);

// Get the image compose
$compose =  $gmagick->getimagecompose();
echo $compose;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagecompose.php](https://www.php.net/manual/en/gmagick.getimagecompose.php)