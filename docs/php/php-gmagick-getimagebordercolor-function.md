# PHP|Gmagick getimagebordercolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagebordercolor-function/](https://www.geeksforgeeks.org/php-gmagick-getimagebordercolor-function/)

**gmagick：：getimagebordercolor()函数**是 PHP 中的一个内置函数，用于获取图像边框颜色。

**语法：**

```php
*Gmagickpixel* Gmagick::getimagebordercolor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含颜色的 GmagickPixel 对象。

**异常：**此函数在出错时引发 GmagickException。

**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**Gmagick：：getimagebordercolor()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the border color
$color = $gmagick->getimagebordercolor();
print("<pre>".print_r($color->getcolor(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(57311, 57311, 57311) // which is the default border color.
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the border color
$gmagick->setimagebordercolor('#8c7f5b');

// Get the border color
$color = $gmagick->getimagebordercolor();
print("<pre>".print_r($color->getcolor(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(35980, 32639, 23387)
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagebordercolor.php](https://www.php.net/manual/en/gmagick.getimagebordercolor.php)