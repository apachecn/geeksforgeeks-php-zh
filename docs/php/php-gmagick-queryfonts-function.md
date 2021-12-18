# PHP|Gmagick 查询字体()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-queryfonts-function/](https://www.geeksforgeeks.org/php-gmagick-queryfonts-function/)

**Gmagick：：queryfonts()函数**是 PHP 中的一个内置函数，用于获取配置的字体。

**语法：**

```php
*array* Gmagick::queryfonts( *string* $pattern )
```

**参数：**此函数接受单个参数**$Pattern**，该参数包含要获取字体的正则表达式，请使用‘*’获取所有字体。

**返回值：**此函数返回包含字体的数组值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：queryfonts()函数**：

**程序 1(获取所有可用字体)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Get all the fonts
$fonts = $gmagick->queryfonts('*');
foreach ($fonts as $font) {
    echo $font . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(获取特定字体)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Get fonts with names starting from Times
$fonts = $gmagick->queryfonts('Times*');

foreach ($fonts as $font) {
    echo $font . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.queryfonts.php](https://www.php.net/manual/en/gmagick.queryfonts.php)