# PHP|Gmagick getimagegreenprimary()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagegreenprimary-function/](https://www.geeksforgeeks.org/php-gmagick-getimagegreenprimary-function/)

**gmagick：：getimagegreenprimary()函数**是 PHP 中的一个内置函数，用于返回色度绿色基准点。 此函数返回一个具有键“x”和“y”的数组。

**语法：**

```php
*array* Gmagick::getimagegreenprimary( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含点的 x 和 y 坐标的数组值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagegreenprimary()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Use the getimagegreenprimary() function
$res = $gmagick->getimagegreenprimary();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Use the setimagegreenprimary() function
$gmagick->setimagegreenprimary(6, 8);

// Use the getimagegreenprimary() function
$res = $gmagick->getimagegreenprimary();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagegreenprimary.php](https://www.php.net/manual/en/gmagick.getimagegreenprimary.php)