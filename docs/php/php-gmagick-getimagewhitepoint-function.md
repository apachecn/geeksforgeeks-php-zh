# PHP|Gmagick getimageWhitepoint()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagewhitepoint-function/](https://www.geeksforgeeks.org/php-gmagick-getimagewhitepoint-function/)

**Gmagick：：getimageWhitepoint()函数**是 PHP 中的一个内置函数，用于将色度白点作为具有键“x”和“y”的关联数组来获取。

**语法：**

```php
*array* Gmagick::getimagewhitepoint( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含色度白点的数组值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageWhitepoint()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new  Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the white point
$res = $gmagick->getimagewhitepoint();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [x] => 0.31270000338554
    [y] => 0.3289999961853
)
```

**程序 2：**

```php
<?php

// Create a new  Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the white point
$gmagick->setimagewhitepoint(5, 5);

// Get the white point
$res = $gmagick->getimagewhitepoint();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [x] => 5
    [y] => 5
)
```

**引用：**[https://www.php.net/manual/en/gmagick.getimagewhitepoint.php](https://www.php.net/manual/en/gmagick.getimagewhitepoint.php)