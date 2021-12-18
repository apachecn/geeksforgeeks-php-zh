# PHP|Imagick getFilename()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getfilename-function/](https://www.geeksforgeeks.org/php-imagick-getfilename-function/)

**Imagick：：getFilename()函数**是 PHP 中的一个内置函数，用于获取与图像序列相关联的文件名。

**语法：**

```php
*string* Imagick::getFilename( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数在成功时返回字符串值。

下面的程序演示了 PHP 中的**Imagick：：getFilename()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Filename
$name = $imagick->getFilename();

echo $name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Filename
$imagick->setFilename('myimage.png');

// Get the Filename
$name = $imagick->getFilename();

echo $name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getfilename.php](https://www.php.net/manual/en/imagick.getfilename.php)