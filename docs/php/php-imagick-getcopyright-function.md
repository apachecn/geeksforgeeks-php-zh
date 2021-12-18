# PHP|Imagick getCopyright()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getcopyright-function/](https://www.geeksforgeeks.org/php-imagick-getcopyright-function/)

**Imagick：：getCopyright()**函数是 PHP 中的一个内置函数，用于返回当前 ImageMagick API 版权，该版权用作字符串。

**语法：**

```php
*string* Imagick::getCopyright( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个字符串，其中包含 ImageMagick 和 Magickwand C API 的版权声明。

下面的程序演示了 PHP 中的**Imagick：：getCopyright()**函数()：

**程序：**

```php
<?php 
/*require_once('vendor/autoload.php');*/ 

/*Imagick Object*/

$image = new \Imagick();

/*Copyright of current Imagick Library*/

$string = $image->getCopyright();

/*String*/

echo $string;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/imagick.getcopyright.php](http://php.net/manual/en/imagick.getcopyright.php)