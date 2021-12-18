# PHP|Imagick getImageProperty()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageproperty-function/](https://www.geeksforgeeks.org/php-imagick-getimageproperty-function/)

**Imagick：：getImageProperty()函数**是 PHP 中的内置函数，用于获取图像属性。 图像属性和图像工件之间的主要区别在于属性是公共的，而工件是私有的。

**语法：**

```php
*string* Imagick::getImageProperty( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数在成功时返回属性值。

下面的程序演示了 PHP 中的**Imagick：：getImageProperty()函数**：

**程序：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the setImageProperty() function
$imagick->setImageProperty("property_name", "property_value");

// Apply the getImageProperty() function
$property_name = $imagick->getImageProperty("property_name");
echo $property_name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageproperty.php](https://www.php.net/manual/en/imagick.getimageproperty.php)