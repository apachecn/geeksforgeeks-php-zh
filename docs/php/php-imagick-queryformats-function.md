# PHP|Imagick queryFormats()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-queryformats-function/](https://www.geeksforgeeks.org/php-imagick-queryformats-function/)

**Imagick：：queryFormats()函数**是 PHP 中的一个内置函数，用于获取 Imagick 支持的格式。

**语法：**

```php
*array* Imagick::queryFormats( *string* $pattern = "*" )
```

**参数：**此函数接受单个参数**$pattern**，该参数保存要与格式匹配的模式。

**返回值：**此函数返回包含 Imagick 支持的格式的数组。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：queryFormats()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get all the formats
$formats =  $imagick->queryFormats('*');
print("<pre>".print_r($formats, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get all the formats with pattern related to 'PNG'
$formats =  $imagick->queryFormats('PNG*');
print("<pre>".print_r($formats, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.queryformats.php](https://www.php.net/manual/en/imagick.queryformats.php)