# PHP|SplFileObject fgets()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fgets-function/](https://www.geeksforgeeks.org/php-splfileobject-fgets-function/)

**SplFileObject：：fgets()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，从文件中获取行的值为 USD。

**语法：**

```php
string SplFileObject::fgets( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件下一行的字符串，否则返回 False。

下面的程序演示了 PHP 中的 SplFileObject：：fgets()函数。

**程序 1：**

```php
<?php

// Creating SplFile Object
$gfg = new SplFileObject("gfg.txt");
while (!$gfg->eof()) {
    echo $gfg->fgets();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Creating SplFile Object
$gfg = new SplFileObject(__FILE__);
while (!$gfg->eof()) {
    echo $gfg->fgets();
}
?>
```

**输出：**

```php
<?php

// Creating SplFile Object
$gfg = new SplFileObject(__FILE__);
while (!$gfg->eof()) {
    echo $gfg->fgets();
}
?>

```

**引用：**[http://php.net/manual/en/splfileobject.fgets.php](http://php.net/manual/en/splfileobject.fgets.php)