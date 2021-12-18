# PHP|Imagick setPage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setpage-function/](https://www.geeksforgeeks.org/php-imagick-setpage-function/)

**Imagick：：setPage()函数**是 PHP 中的一个内置函数，用于设置 Imagick 对象的页面几何。

**语法：**

```php
*bool* Imagick::setPage( *int* $width, *int* $height, *int* $x, *int* $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width:** it specifies the width of the page.
*   **$Height:** it specifies the height of the page.
*   **$x:** it specifies the x coordinates of the page.
*   **$y:** it specifies the y coordinates of the page.

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setPage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Page Geometry
$imagick->setPage(220, 350, 0, 5);

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
$imagick->setPage(200, 100, 8, 16);

// Get the Page Geometry
$geometry = $imagick->getPage();
print_r($geometry);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setpage.php](https://www.php.net/manual/en/imagick.setpage.php)