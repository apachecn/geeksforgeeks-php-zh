# PHP|Imagick setSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setsize-function/](https://www.geeksforgeeks.org/php-imagick-setsize-function/)

**Imagick：：setSize()函数**是 PHP 中的一个内置函数，用于设置与 Imagick 对象相关联的大小。

**语法：**

```
*bool* Imagick::setSize( *int* $columns, *int* $rows )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$Columns:** it specifies the width in pixels.
*   **$row:** it specifies the height in pixels.

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setSize()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size
$imagick->setSize('500', '800');

// Get the size
$size = $imagick->getSize();
print("<pre>".print_r($size, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size
$imagick->setSize('250', '900');

// Get the size
$size = $imagick->getSize();
print("<pre>".print_r($size, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setsize.php](https://www.php.net/manual/en/imagick.setsize.php)