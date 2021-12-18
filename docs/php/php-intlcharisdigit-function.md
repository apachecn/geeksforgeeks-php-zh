# PHP|IntlChar：：isdigit()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisdigit-function/](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)

**IntlChar：：isdigit()**函数是 PHP 中的一个内置函数，用于确定给定的输入代码数据是否为数字字符。 当字符在一般类别的十进制数字下时，它返回 TRUE。 从 Unicode 4 开始，这与测试 Decimal 的 Numerical_Type 相同。

**语法：**

```
*bool* IntlChar::isdigit ( $codepoint )
```

**参数：**此函数接受上述单个参数，如下所述：

*   **$codepoint：**输入参数$input_codepoint 是一个整数或字符，编码为*UTF-8*字符串。

**返回值：**如果$codepoint 数据是数字字符，则返回 True，否则返回 False。
示例：

```
Input : $codepoint = "X"
Output : bool(false)

Input : $codepoint = "7"
Output : bool(true)
```

以下程序说明 PHP：
**程序 1：**中的**IntlChar：：isdigit()**函数

## PHP

```
<?php
// PHP code to illustrate the
// IntlChar::isdigit() function.

// single digit
var_dump(IntlChar::isdigit("5"));

// number cases
var_dump(IntlChar::isdigit("5555"));

// float number
var_dump(IntlChar::isdigit("15.08"));

// big number
var_dump(IntlChar::isdigit("12e"));
?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(true)
NULL 
NULL 
NULL
```

**程序 2：**

## PHP

```
<?php
// PHP code to illustrate the
// IntlChar::isdigit() function.

// alphabet cases
var_dump(IntlChar::isdigit("G"));

// in space cases
var_dump(IntlChar::isdigit(" "));

// new line cases
var_dump(IntlChar::isdigit("\n"));

// string cases
var_dump(IntlChar::isdigit("Geeks "));

// symbol cases
var_dump(IntlChar::isdigit("@"));

?>
```

发帖主题：Re：Колибри0.7.0

```
bool(false) 
bool(false) 
bool(false) 
NULL 
bool(false)
```

**程序 3：**

## PHP

```
<?php
// PHP code to illustrate the
// IntlChar::isdigit() function.

var_dump(IntlChar::isdigit("0"));

var_dump(IntlChar::isdigit(' '));
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true) 
bool(false)
```

**引用：**[http://php.net/manual/en/intlchar.isdigit.php](http://php.net/manual/en/intlchar.isdigit.php)