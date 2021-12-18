# PHP|is_scalar()函数

> Original: [https://www.geeksforgeeks.org/php-is_scalar-function/](https://www.geeksforgeeks.org/php-is_scalar-function/)

Is_scalar()函数是 PHP 中的内置函数，用于检查变量是否为标量。

**语法：**

```php
*bool* is_scalar ( $var )
```

**参数：**此函数接受单个参数，如以上语法和所述，如下所述。

*   **$var:** variable to check if it is scalar.

**返回值：**当$var 为标量时返回 TRUE，否则返回 FALSE。

**注：**

*   包含布尔型、双精度型、整型或字符串类型的变量是标量。
*   数组、对象和资源不是标量。
*   Is_scalar()不认为 NULL 是标量。

下面的程序演示了 PHP 中的 is_scalar()函数：

```php
<?php

// PHP code to demonstrate the working of
// is_scalar() function

$var1 = true; // boolean value 
var_dump(is_scalar($var1));

$var2 = 3; // integer value
var_dump(is_scalar($var2));

$var3 = 5.6; // double value
var_dump(is_scalar($var3));

$var4 = "Abc3462"; // string value
var_dump(is_scalar($var4));

$var5 = array(1, 2, 3); // array value
var_dump(is_scalar($var5));

$var6 = new stdClass; // object value
var_dump(is_scalar($var6));

$var7 = tmpfile(); // resource value
var_dump(is_scalar($var7));
?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)

```

**引用：**[http://php.net/manual/en/function.is-scalar.php](http://php.net/manual/en/function.is-scalar.php)