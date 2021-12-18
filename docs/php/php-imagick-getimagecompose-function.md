# PHP|Imagick getImageCompose()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagecompose-function/](https://www.geeksforgeeks.org/php-imagick-getimagecompose-function/)

**Imagick：：getImageCompose()函数**是 PHP 中的一个内置函数，用于获取与图像相关联的复合运算符。

**语法：**

```php
*int* Imagick::getImageCompose( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：getImageCompose()函数**：

**程序 1：**

```php
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Compose
$compose = $imagick->getImageCompose();
echo $compose;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compose
$imagick->setImageCompose(70);

// Get the Compose
$compose = $imagick->getImageCompose();
echo $compose;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagecompose.php](https://www.php.net/manual/en/imagick.getimagecompose.php)