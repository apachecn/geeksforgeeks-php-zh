# PHP|Gmagick getfilename()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getfilename-function/](https://www.geeksforgeeks.org/php-gmagick-getfilename-function/)

**Gmagick：：getfilename()函数**是 PHP 中的一个内置函数，用于获取与 Gmagick 对象中的图像相关联的文件名。

**语法：**

```php
*string* Gmagick::getfilename( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件名的字符串值。

**异常：**此函数在出错时引发 GmagickException。

**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序说明了 PHP：
**程序 1：**中的**Gmagick：：getfilename()函数**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick(
    'geeksforgeeks.png');

// Get the filename
$filename = $gmagick->getfilename();
echo $filename;  
?>  
```

发帖主题：Re：Колибри0.7.0

```php
This will give empty string which is default name for all images.
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick(
    'geeksforgeeks.png');

// Set the filename
$gmagick->setfilename('geeksforgeeks.png');

// Get the filename
$filename = $gmagick->getfilename();
echo $filename;  
?>  
```

发帖主题：Re：Колибри0.7.0

```php
geeksforgeeks.png
```

**引用：**[https://www.php.net/manual/en/gmagick.getfilename.php](https://www.php.net/manual/en/gmagick.getfilename.php)