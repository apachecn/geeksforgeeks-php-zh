# PHP|Doubleval()函数

> Original: [https://www.geeksforgeeks.org/php-doubleval-function/](https://www.geeksforgeeks.org/php-doubleval-function/)

Doubleval()是 PHP 中的一个内置函数，用于获取变量的浮点值。 此函数是[Floatval()](https://www.geeksforgeeks.org/php-floatval-function/)的别名。

**语法：**

```php
doubleval ( $variable_name )
```

**参数：**此函数接受一个参数*$VARIABLE_NAME*，如上面的语法所示。 这是必选参数。 此参数指定要转换的变量的名称。 此参数可以是混合类型，例如整数、字符串等。

**返回值：**返回给定变量的浮点值。

以下程序说明了在 PHP：
**程序 1：**中使用 doubleval()函数的方法

```php
<?php

// PHP program to illustrate 
// doubleval() function
$var = '41.68127E3';
$double_value = doubleval($var);
echo $double_value;
?>
```

**Output:**

```php
41681.27

```