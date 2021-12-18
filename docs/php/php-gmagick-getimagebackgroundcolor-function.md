# PHP|Gmagick getimagebackround color()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagebackgroundcolor-function/](https://www.geeksforgeeks.org/php-gmagick-getimagebackgroundcolor-function/)

**gmagick：：getimagebackround color()函数**是 PHP 中的一个内置函数，用于获取图像背景颜色。

**语法：**

```php
*Gmagickpixel* Gmagick::getimagebackgroundcolor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含颜色的 Gmagickxent 值。

**异常：**此函数在出错时引发 GmagickException。

**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**Gmagick：：getimagebackround color()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the background color
$color = $gmagick->getimagebackgroundcolor();
print("<pre>".print_r($color->getcolor(), true)."</pre>");
?>  
```

发帖主题：Re：Колибри0.7.0

```php
rgb(65535, 65535, 65535)  // Which is the default image background color.
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the background color
$gmagick->setimagebackgroundcolor('#ba5959');

// Get the background color
$color = $gmagick->getimagebackgroundcolor();
print("<pre>".print_r($color->getcolor(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(47802, 22873, 22873)
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagebackgroundcolor.php](https://www.php.net/manual/en/gmagick.getimagebackgroundcolor.php)