# PHP|Gmagick getimagemattecolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagemattecolor-function/](https://www.geeksforgeeks.org/php-gmagick-getimagemattecolor-function/)

**gmagick：：getimagemattecolor()函数**是 PHP 中的一个内置函数，用于获取图像的哑光颜色。

**语法：**

```php
*GmagickPixel* Gmagick::getimagemattecolor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含遮罩颜色的 GmagickPixel 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagemattecolor()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the matte color
$colorPixel = $gmagick->getimagemattecolor();
echo $colorPixel->getcolor();
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(48573, 48573, 48573)
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the matte color
$gmagick->setimagemattecolor('green');

// Get the matte color
$colorPixel = $gmagick->getimagemattecolor();
echo $colorPixel->getcolor();
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(0, 32896, 0)
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagemattecolor.php](https://www.php.net/manual/en/gmagick.getimagemattecolor.php)