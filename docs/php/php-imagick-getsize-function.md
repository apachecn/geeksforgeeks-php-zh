# PHP|Imagick getSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getsize-function/](https://www.geeksforgeeks.org/php-imagick-getsize-function/)

**Imagick：：getSize()函数**是 PHP 中的一个内置函数，用于获取与 Imagick 对象相关联的大小。

**语法：**

```php
*array* Imagick::getSize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个具有键“Columns”和“Rows”的数组。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getSize()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the size
$size = $imagick->getSize();
print("<pre>".print_r($size, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size
$imagick->setSize('200', '400');

// Get the size
$size = $imagick->getSize();
print("<pre>".print_r($size, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getsize.php](https://www.php.net/manual/en/imagick.getsize.php)