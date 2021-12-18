# PHP|Gmagick getimagetype()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagetype-function/](https://www.geeksforgeeks.org/php-gmagick-getimagetype-function/)

**gmagick：：getimagetype()函数**是 PHP 中的一个内置函数，用于获取图像类型。

**语法：**

```
*int* Gmagick::getimagetype( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与[IMGTYPE 常量之一](https://www.php.net/manual/en/gmagick.constants.php#gmagick.constants.imgtype-undefined)对应的整数值。
下面列出了所有 IMGTYPE 常量：

*   Gmagick：：IMGTYPE_UNDEFINED(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Gmagick：：IMGTYPE_GRAYSCALE(2)
*   Gmagick：：IMGTYPE_GRAYSCALEMATTE(3)
*   Gmagick：：IMGTYPE_Palette(4)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   GMAGICK：：IMGTYPE_TRUECOLOR(6)
*   GMAGICK：：IMGTYPE_TRUECOLORMATTE(7)
*   GMAGICK：：IMGTYPE_COLORSEPARATION(8)
*   GMAGICK：：IMGTYPE_COLORSEPARATIONMATTE(9)
*   GMAGICK：：IMGTYPE_OPTIMIZE(10)

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagetype()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new  Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Use getimagetype function
$res = $gmagick->getimagetype();
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
6 // Which corresponds to gmagick::IMGTYPE_TRUECOLOR.
```

**程序 2：**

```
<?php

// Create a new  Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the Image Type 
$gmagick->setImageType(Gmagick::IMGTYPE_PALETTE); 

// Use getimagetype function
$res = $gmagick->getimagetype();
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
4
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagetype.php](https://www.php.net/manual/en/gmagick.getimagetype.php)