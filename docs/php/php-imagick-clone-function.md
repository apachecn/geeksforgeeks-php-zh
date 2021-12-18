# PHP|Imagick clone()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-clone-function/](https://www.geeksforgeeks.org/php-imagick-clone-function/)

Imagick：：Clone()函数是 PHP 中的内置函数，用于创建 Imagick 对象的副本。 此函数创建同一实例的副本，这意味着它将具有相同的属性，其中的任何更改都不会反映到主对象。

**语法：**

```php
*Imagick* Imagick::clone( void )
```

**参数：**此函数不接受任何参数。

**返回值：**它返回 Imagick 对象的副本。

下面的程序演示了 PHP 中的 Imagick：：Clone()函数：

**程序：**

```php
<?php

// Create new Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Use clone() function to copy the image
$im_clone = clone $image;

header("Content-Type: image/gif");

// Display the image
echo $im_clone->getImagesBlob();

?>
```

**输出：**
![clone image](img/809ba4c1b8a40f7d6160dcba9cd06fd3.png)

**引用：**[https://www.php.net/manual/en/imagick.clone.php](https://www.php.net/manual/en/imagick.clone.php)