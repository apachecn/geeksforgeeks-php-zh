# PHP|SplFileObject fstat()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fstat-function/](https://www.geeksforgeeks.org/php-splfileobject-fstat-function/)

SplFileObject：：fstat()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于提供文件信息。

**语法：**

```php
*array* SplFileObject::fstat( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件详细信息的数组。

下面的程序演示了 PHP 中的 SplFileObject：：fstat()函数：

**程序 1：**

```php
<?php

// Create an SplFile Object 
$gfg = new SplFileObject("gfg.txt", "r");

$stat = $gfg->fstat();

// Print result
print_r($stat);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**提供当前文件信息的 PHP 程序。

```php
<?php

// Create Spl Object 
$gfg = new SplFileObject(__FILE__, "r");

$stat = $gfg->fstat();

// Print result
print_r($stat);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/splfileobject.fstat.php](http://php.net/manual/en/splfileobject.fstat.php)