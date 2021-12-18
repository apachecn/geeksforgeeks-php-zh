# PHP|hrtime()函数

> Original: [https://www.geeksforgeeks.org/php-hrtime-function/](https://www.geeksforgeeks.org/php-hrtime-function/)

函数**hrtime()**是 PHP 中的一个内置函数，它返回系统的高精度时间。

**语法：**

```
*mixed* hrtime( *bool* $is_num_return );
```

**参数：**此函数接受单个参数，如上所述，如下所述：

*   **$is_num_return:** it is an optional parameter of type boolean. It specifies whether it is returned as a single number or an array. If set to TRUE, numbers are returned, and if set to FALSE, an array of integers is returned. The default value is False.

**返回值：**此函数返回纳秒或整数数组。

**注意：**此函数适用于 PHP 7.3.0 及更高版本。

以下程序说明了 PHP 中的**hrtime()函数**：

**程序 1：**此程序将**$IS_NUM_RETURN**设置为 TRUE。

```
<?php
print_r(hrtime(TRUE));
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**此程序不设置**$IS_NUM_RETURN**值。 这意味着它采用默认值。

```
<?php
print_r(hrtime());
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.hrtime.php](https://www.php.net/manual/en/function.hrtime.php)