# PHP|Imagick setFilename()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setfilename-function/](https://www.geeksforgeeks.org/php-imagick-setfilename-function/)

**Imagick：：setFilename()函数**是 PHP 中的一个内置函数，用于在读取或写入图像之前设置文件名。

**语法：**

```php
*bool* Imagick::setFilename( *string* $filename )
```

**参数：**此函数接受单个参数**$filename**，该参数保存表示文件名的字符串。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setFilename()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Filename
$imagick->setFilename('myNewFilename.png');

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
$imagick->setFilename('myAnotherNewFilename.png');

// Get the Filename
$name = $imagick->getFileName();

// Write the image to same folder
$imagick->writeImage($name);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setfilename.php](https://www.php.net/manual/en/imagick.setfilename.php)