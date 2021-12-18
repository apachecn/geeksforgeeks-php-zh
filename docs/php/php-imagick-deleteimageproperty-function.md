# PHP|Imagick delete eImageProperty()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-deleteimageproperty-function/](https://www.geeksforgeeks.org/php-imagick-deleteimageproperty-function/)

**Imagick：：delete eImageProperty()函数**是 PHP 中的内置函数，用于删除图像属性。 图像属性和图像工件之间的主要区别在于属性是公共的，而工件是私有的。

**语法：**

```php
*bool* Imagick::deleteImageProperty( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：delete eImageProperty()函数**：

**程序：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the setImageProperty() function to create a property
$imagick->setImageProperty("property_name", "property_value");

// Apply the deleteImageProperty() function to delete that property
$imagick->deleteImageProperty("property_name");

?>
```

**输出：**
此程序删除图像属性

**引用：**[https://www.php.net/manual/en/imagick.deleteimageproperty.php](https://www.php.net/manual/en/imagick.deleteimageproperty.php)