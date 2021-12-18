# PHP|Floatval()函数

> Original: [https://www.geeksforgeeks.org/php-floatval-function/](https://www.geeksforgeeks.org/php-floatval-function/)

Floatval()函数是 PHP 中的内置函数，它返回变量的浮点值。

**语法：**

```php
float floatval ( $var )

```

**参数：**此函数接受一个必选参数，如下所述：

*   **$var：**将返回其对应浮点值的变量。 此变量不应为对象。

**返回值：**返回给定变量的浮点值。 空数组返回 0，非空数组返回 1。

**注意：**如果将对象传递给函数，则会产生**E_NOTICE**级别错误并返回 1。

例如：

```php
Input : $var = '41.68127E3'
Output : 41681.27

Input : $var = '47.129mln'
Output : 47.129

```

以下程序说明了 PHP：
**程序 1：**中的 Floatval()函数的用法

```php
<?php
$var = '41.68127E3';
$float_value = floatval($var);
echo $float_value;
?>
```

**Output:**

```php
41681.27

```

**程序 2：**

```php
<?php
$var = '47.129mln';
$float_value = floatval($var);
echo $float_value;
?>
```

**Output:**

```php
47.129

```

**引用：**[http://php.net/manual/en/function.floatval.php](http://php.net/manual/en/function.floatval.php)