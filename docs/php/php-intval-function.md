# PHP|intval()函数

> Original: [https://www.geeksforgeeks.org/php-intval-function/](https://www.geeksforgeeks.org/php-intval-function/)

Intval()函数是 PHP 中的内置函数，它返回变量的整数值。

**语法：**

```
int intval ( $var, $base )

```

**参数：**此函数接受两个参数，其中一个是必选的，另一个是可选的。 参数说明如下：

*   **$var:** is a required parameter and is used as a variable that needs to be converted to an integer value.
*   **$BASE:** this is an optional parameter that specifies the cardinality of the conversion of $var to its corresponding integer. If $BASE is not specified,.
    *   If *$var* contains 0x (or 0x) as the prefix, the cardinality is 16.
    *   If *$var* starts with 0, the cardinality is 8
    *   Otherwise, the cardinality is 10

**返回值：**返回$var 对应的整数值。

**示例：**

```
Input : $var = '120', $base = 8
Output : 80

Input : $var = 0x34
Output : 52

Input : $var = 034
Output : 28

```

以下程序说明了如何在 PHP 中使用 intval()函数：

**程序 1：**

```
<?php
$var = '7.423';
$int_value = intval($var);
echo $int_value;
?>
```

**输出：**

```
7

```

**程序 2：**

```
<?php
$var = 0x423;
$int_value = intval($var);
echo $int_value;
?>
```

**输出：**

```
1059

```

**程序 3：**

```
<?php
$var = "64";
echo intval($var)."\n".intval($var, 8);

?>
```

**输出：**

```
64
52

```

**引用：**[http://php.net/manual/en/function.intval.php](http://php.net/manual/en/function.intval.php)