# PHP|Imagick getImageGreenPrimary()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagegreenprimary-function/](https://www.geeksforgeeks.org/php-imagick-getimagegreenprimary-function/)

**Imagick：：getImageGreenPrimary()**函数是 PHP 中的内置函数，用于返回色度绿色基准点。 此函数返回一个具有键“x”和“y”的数组。

**语法：**

```php
*array* Imagick::getImageGreenPrimary( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个包含点的 x 和 y 坐标的数组。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageGreenPrimary()**函数：

**程序 1：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use getImageGreenPrimary function
$res = $imagick->getImageGreenPrimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Use setImageGreenPrimary function
$imagick->setImageGreenPrimary(12, 19);

// Use getImageGreenPrimary function
$res = $imagick->getImageGreenPrimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagegreenprimary.php](https://www.php.net/manual/en/imagick.getimagegreenprimary.php)