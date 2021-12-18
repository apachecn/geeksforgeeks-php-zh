# PHP|var_export()函数

> Original: [https://www.geeksforgeeks.org/php-var_export-function/](https://www.geeksforgeeks.org/php-var_export-function/)

Var_export()是 PHP 中的一个内置函数，用于返回作为参数传递给此函数的变量的结构化值(信息)。 此函数类似于[var_dump()函数](https://www.geeksforgeeks.org/php-var_dump-function/)。
**语法**：

```
var_export($var, $return)
```

**参数**：此函数接受上述语法中所示的两个参数，如下所示：

*   **$var**：该参数表示要导出的变量。
*   **$return**：这是一个可选参数，属于布尔型。 如果使用它并将其设置为 true，则此函数返回变量表示形式，而不是输出它。 此参数的默认值为 False。

**返回类型**：如果使用$return 参数，则返回变量表示形式，否则设置为 true，否则此函数返回 NULL。
以下程序说明了 var_export()函数：
**程序 1**：

## PHP

```
<?php
// PHP program to illustrate
// the var_export() function

$var = '11.89';

$res = var_export($var, true);

echo $res;

?>
```

输出：0

```
'11.89'
```

**程序 2**：

## PHP

```
<?php
// PHP program to illustrate
// the var_export() function

$var = +11.99;

$res = var_export($var);

echo $res ;

?>
```

输出：0

```
11.99
```

**参考**：
[http://php.net/manual/en/function.var-export.php](http://php.net/manual/en/function.var-export.php)