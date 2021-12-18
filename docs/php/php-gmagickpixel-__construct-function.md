# PHP|GmagickPixel__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickpixel-__construct-function/](https://www.geeksforgeeks.org/php-gmagickpixel-__construct-function/)

**GmagickPixel：：__Construct()函数**是 PHP 中的内置函数，用于构造 GmagickPixel 对象。 如果指定了颜色，则对象将被构造，然后在返回之前使用该颜色进行初始化。

**语法：**

```
*GmagickPixel* GmagickPixel::__construct( *string* $color )
```

**参数：**此函数接受单个参数**$color**，该参数是可选的，并保持颜色。

**返回值：**此函数成功时返回 GmagickPixel 对象。

**异常：**此函数在出错时引发 GmagickPixelException。

下面给出的程序演示了 PHP 中的**GmagickPixel：：__Construct()函数**：

**程序 1(无颜色参数)：**

```
<?php

// Create a new GmagickPixel
// object using __construct
$gmagickPixel = new GmagickPixel();

// Get the color
$color = $gmagickPixel->getcolor();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(带颜色参数)：**

```
<?php

// Create a new GmagickPixel object
// using __construct
$gmagickPixel = new GmagickPixel('#ccb062');

// Get the color
$color = $gmagickPixel->getcolor();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagickpixel.construct.php](https://www.php.net/manual/en/gmagickpixel.construct.php)