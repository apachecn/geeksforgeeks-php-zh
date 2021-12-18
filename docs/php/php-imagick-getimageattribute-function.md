# PHP|Imagick getImageAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageattribute-function/](https://www.geeksforgeeks.org/php-imagick-getimageattribute-function/)

**Imagick：：getImageAttribute()函数**是 PHP 中的一个内置函数，用于获取键的命名属性。

**语法：**

```php
*string* Imagick::getImageAttribute( *string* $key )
```

**参数：**此函数接受单个参数**$key**，该参数以字符串格式保存键值。

**返回值：**此函数在成功时返回字符串值。

下面的程序说明了 PHP 中的**Imagick：：getImageAttribute()函数**：

**程序 1：**

```php
<?php

// Create a Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the attribute with key 'hello'
$attribute = $imagick->getImageAttribute('hello');

echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set an attribute with key 'hello'
$imagick->setImageAttribute('hello', 'world');

// Get the attribute with key 'hello'
$attribute = $imagick->getImageAttribute('hello');

echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageattribute.php](https://www.php.net/manual/en/imagick.getimageattribute.php)