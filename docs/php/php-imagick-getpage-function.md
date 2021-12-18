# PHP|Imagick getPage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getpage-function/](https://www.geeksforgeeks.org/php-imagick-getpage-function/)

**Imagick：：getPage()函数**是 PHP 中的一个内置函数，用于以关联数组格式返回与 Imagick 对象相关联的页面的几何形状。

**语法：**

```php
*array* Imagick::getPage( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回具有键“width”、“Height”、“x”和“y”的关联数组。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getPage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Page Geometry
$geometry = $imagick->getPage();

print_r($geometry);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Page Geometry
$imagick->setPage(200, 300, 0, 0);

// Get the Page Geometry
$geometry = $imagick->getPage();

print_r($geometry);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getpage.php](https://www.php.net/manual/en/imagick.getpage.php)