# PHP 中如何将字符串转换为布尔值？

> 原文:[https://www . geesforgeks . org/如何将字符串转换为 php 中的布尔值/](https://www.geeksforgeeks.org/how-to-convert-string-to-boolean-in-php/)

给定一个字符串，任务是将给定的字符串转换成它的布尔值。使用 [filter_var()函数](https://www.geeksforgeeks.org/php-filter_var-function/)将字符串转换为布尔值。

**例:**

```
Input  : $boolStrVar1 = filter_var('true', FILTER_VALIDATE_BOOLEAN); 
Output : true

Input  : $boolStrVar5 = filter_var('false', FILTER_VALIDATE_BOOLEAN);
Output : false

```

**使用 PHP filter_var()函数的方法:**filter _ var()函数用于过滤具有指定过滤器的变量。此功能用于验证和清理数据。

**语法:**

```
filter_var( var, filterName, options )
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **var:** 为必填字段。它表示要过滤的变量。
*   **过滤器名称:**用于指定要使用的过滤器的 ID 或名称。默认过滤器是 FILTER_DEFAULT。它是可选字段。
*   **选项:**用于指定要使用的一个或多个标志/选项。检查每个过滤器的可能选项和标志。它也是可选字段。

**返回值:**成功返回过滤后的数据，失败返回假。

**程序:**

```
<?php
// PHP program to illustrate the conversion
// of String to Boolean value

// The below statement returns the boolean value true
var_dump(filter_var('true', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('1', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('on', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('yes', FILTER_VALIDATE_BOOLEAN));

// The below statement returns the boolean value false
var_dump(filter_var('false', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('0', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('off', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('no', FILTER_VALIDATE_BOOLEAN));
var_dump(filter_var('', FILTER_VALIDATE_BOOLEAN));

?>
```

**输出:**

```
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)
bool(false)
bool(false)

```