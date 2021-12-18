# PHP|Gmagick getCopyright()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getcopyright-function/](https://www.geeksforgeeks.org/php-gmagick-getcopyright-function/)

**Gmagick：：getCopyright()**函数是 PHP 中的一个内置函数，用于返回包含当前 Gmagick API 版权的字符串。

**语法：**

```php
*string* Gmagick::getcopyright( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个字符串，其中包含 GraphicsMagick 和 Magickwand C API 的版权声明。

**错误/异常：**此函数在出错时引发 GmagickException。

下面的程序说明了 PHP 中的**Gmagick：：getCopyright()**函数：

**程序：**

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(); 

// Use getcopyright() function 
$string = $gmagick->getcopyright();

// Output the string
echo $string; 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
Copyright (C) 2002-2018 GraphicsMagick Group. 
Additional copyrights and licenses apply to this software. 
See http://www.GraphicsMagick.org/www/Copyright.html for details.
```

**引用：**[http://php.net/manual/en/gmagick.getcopyright.php](http://php.net/manual/en/gmagick.getcopyright.php)