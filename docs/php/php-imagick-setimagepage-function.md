# PHP|Imagick setImagePage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagepage-function/](https://www.geeksforgeeks.org/php-imagick-setimagepage-function/)

**Imagick：：setImagePage()函数**是 PHP 中的一个内置函数，用于设置图像页面几何图形。

**语法：**

```php
*bool* Imagick::setImagePage(*int* $width, *int* $height, *int* $x, *int* $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$width:** it specifies the width of the image page.
*   **$Height:** specifies the height of the picture page.
*   **$x:** it specifies x coordinates.
*   **$y:** it specifies y coordinates.

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImagePage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Page
$imagick->setImagePage(100, 400, 0, 0);

// Get the Image Page
$geometry = $imagick->getImagePage();

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

// Set the Image Page
$imagick->setImagePage(300, 200, 20, 50);

// Get the Image Page
$geometry = $imagick->getImagePage();

print_r($geometry);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimagepage.php](https://www.php.net/manual/en/imagick.setimagepage.php)