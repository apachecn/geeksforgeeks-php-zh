# PHP|Gmagick setimagebordercolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagebordercolor-function/](https://www.geeksforgeeks.org/php-gmagick-setimagebordercolor-function/)

**gmagick：：setimagebordercolor()函数**是 PHP 中的一个内置函数，用于设置要应用的图像边框颜色。

**语法：**

```php
*Gmagick* Gmagick::setimagebordercolor( *GmagickPixel* $color )
```

**参数：**此函数接受保存颜色的单个参数**$color**。

**返回值：**此函数在成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimagebordercolor()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the border color
$gmagick->setimagebordercolor('#ba5959');

// Get the border color
$color = $gmagick->getimagebordercolor();
print("<pre>" . print_r($color->getcolor(), true) . "</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
rgb(47802, 22873, 22873)
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the color of border
$gmagick->setimagebordercolor('red');

// Add border
$gmagick->borderimage($gmagick->getimagebordercolor(), 10, 10);

// Display the image
header("Content-Type: image/jpg");
echo $gmagick;
?>
```

**输出：**
![](img/deccf39e7e2b0acd22c83c3bf215cdc8.png)

**引用：**[https://www.php.net/manual/en/gmagick.setimagebordercolor.php](https://www.php.net/manual/en/gmagick.setimagebordercolor.php)