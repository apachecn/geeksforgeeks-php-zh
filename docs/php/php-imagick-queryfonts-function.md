# PHP|Imagick queryFonts()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-queryfonts-function/](https://www.geeksforgeeks.org/php-imagick-queryfonts-function/)

**Imagick：：Imagick：：queryFonts**函数是 PHP 中的内置函数，用于返回 Imagick 库的配置字体。

**语法：**

```php
*array* Imagick::queryFonts( $pattern = "*" )
```

**参数：**此函数接受单个参数*$pattern*，它存储查询模式的值。

**返回值：**此函数返回包含所有已配置字体的数组。

下面的程序演示了 PHP 中的**Imagick：：queryFonts()**函数：

**程序 1：**

```php
<?php 

$output = '';
$output .= "Fonts that match 'Times*' are:<br>";

// Imagick Object
$fontList = Imagick::queryFonts( "Times*" );

foreach ($fontList as $fontName) {
    $output .= $fontName;
}

// Output
echo $output; 
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new Imagick object
$im = new Imagick(); 

// Display all fonts
var_dump( $im->queryFonts() ); 
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/imagick.queryfonts.php](http://php.net/manual/en/imagick.queryfonts.php)