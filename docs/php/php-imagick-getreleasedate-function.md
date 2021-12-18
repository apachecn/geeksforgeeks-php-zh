# PHP|Imagick getReleaseDate()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getreleasedate-function/](https://www.geeksforgeeks.org/php-imagick-getreleasedate-function/)

**Imagick：：getReleaseDate()函数**是 PHP 中的内置函数，用于获取 ImageMagick 的发布日期。

**语法：**

```php
*string* Imagick::getReleaseDate( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含发布日期的字符串值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getReleaseDate()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Release date
$releaseDate = $imagick->getReleaseDate();
echo $releaseDate;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Release date
$releaseDate = $imagick->getReleaseDate();
echo date("F j, Y", strtotime($releaseDate));
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getreleasedate.php](https://www.php.net/manual/en/imagick.getreleasedate.php)