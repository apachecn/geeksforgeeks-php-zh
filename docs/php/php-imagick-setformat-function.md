# PHP|Imagick setFormat()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setformat-function/](https://www.geeksforgeeks.org/php-imagick-setformat-function/)

**Imagick：：setFormat()函数**是 PHP 中的内置函数，用于设置 Imagick 对象的格式。

**语法：**

```
*bool* Imagick::setFormat( *string* $format )
```

**参数：**此函数接受保存字符串值的单个参数**$format**。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setFormat()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Format
$imagick->setFormat('png');

// Get the Format
$format = $imagick->getFormat();

echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Format
$imagick->setFormat('jpeg');

// Get the Format
$format = $imagick->getFormat();

echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setformat.php](https://www.php.net/manual/en/imagick.setformat.php)