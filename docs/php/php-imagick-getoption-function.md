# PHP|Imagick getOption()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getoption-function/](https://www.geeksforgeeks.org/php-imagick-getoption-function/)

**Imagick：：getOption()函数**是 PHP 中的一个内置函数，用于获取与指定键相关联的值。

**语法：**

```php
*string* Imagick::getOption( *string* $key )
```

**参数：**此函数接受保存选项名称的单个参数**$key**。

**返回值：**此函数返回包含与键关联的值的字符串值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getOption()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the option with key 'key1'
$option = $imagick->getOption('key1');
echo $option;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the option
$imagick->setOption('key1', 'option1');

// Get the option with key 'key1'
$option = $imagick->getOption('key1');
echo $option;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getoption.php](https://www.php.net/manual/en/imagick.getoption.php)