# PHP|Imagick getRegistry()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getregistry-function/](https://www.geeksforgeeks.org/php-imagick-getregistry-function/)

**Imagick：：getRegistry()函数**是 PHP 中的一个内置函数，用于获取命名键的 StringRegistry 条目，如果未设置，则为 False。

**语法：**

```php
*string* Imagick::getRegistry( *string* $key )
```

**参数：**此函数接受保存密钥的单个参数**$key**。

**返回值：**此函数返回包含与键关联的值的字符串值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getRegistry()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the Registry
$registry = $imagick->getRegistry('key');
echo $registry;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Set the Registry
$imagick->setRegistry('key', 'my_value');

// Get the Registry
$registry = $imagick->getRegistry('key');
echo $registry;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getregistry.php](https://www.php.net/manual/en/imagick.getregistry.php)