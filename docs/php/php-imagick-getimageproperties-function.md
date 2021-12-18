# PHP|Imagick getImageProperties()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageproperties-function/](https://www.geeksforgeeks.org/php-imagick-getimageproperties-function/)

**Imagick：：getImageProperties()函数**是 PHP 中的一个内置函数，用于获取图像属性。

**语法：**

```php
*array* Imagick::getImageProperties( *string* $pattern, *string* $includes_values )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$Pattern:** it specifies the pattern of the attribute name. The default value is *, which returns all properties.
*   **$INCLUDE_VALUES:** it specifies whether only attribute names are returned. Its default value is true. If False, only the property name is returned.

**返回值：**此函数返回包含图像属性或仅包含属性名称的数组。

下面的程序说明了 PHP 中的**Imagick：：getImageProperties()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Properties
$imagick->setImageProperty('property1', 'value1');
$imagick->setImageProperty('property2', 'value2');
$imagick->setImageProperty('hello', 'world');

// Get the Image Profiles without values starting from "pro"
$properties = $imagick->getImageProperties("pro*", false);
print("<pre>".print_r($properties, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Properties
$imagick->setImageProperty('property1', 'value1');
$imagick->setImageProperty('property2', 'value2');

// Get the Image Profiles
$properties = $imagick->getImageProperties("*");
print("<pre>".print_r($properties, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageproperties.php](https://www.php.net/manual/en/imagick.getimageproperties.php)