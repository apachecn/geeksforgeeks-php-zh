# PHP|lcfirst()函数

> Original: [https://www.geeksforgeeks.org/php-lcfirst-function/](https://www.geeksforgeeks.org/php-lcfirst-function/)

**lcfirst()**函数是 PHP 中的一个内置函数，它接受一个字符串作为参数，并返回第一个字符为小写的字符串，而所有其他字符保持不变。

**语法：**

```
lcfirst($string)
```

**参数：**该函数只接受一个必选参数*$string*。 此参数表示其第一个字符将更改为小写的输入字符串。

**返回值：**该函数仅通过将传递的参数*$string 的第一个字符更改为小写才返回相同的字符串。*

例如：

```
Input : "Geeks for geeks"
Output : geeks for geeks

Input : "chetna agarwal"
Output : chetna agarwal

```

下面的程序演示了 PHP 中的 lcfirst()函数：

**程序 1：**

```
<?php
    // PHP program to demonstrates the 
    // use of lcfirst() function 

    $str = "Geeks for geeks";

    // converts the first character to 
    // lower case and prints the string
    echo(lcfirst($str)); 
?>
```

产出：

```
geeks for geeks

```

**程序 2：**下面的程序演示了在起始字符已经是小写时如何使用 lcfirst()函数。

```
<?php
    // PHP program that demonstrates the 
    // use of lcfirst() function when 
    // the first case is already in lowercase

    $str = "chetna agarwal";

    // already the first character is in lower case 
    // so prints the same string only
    echo(lcfirst($str)); 
?>
```

产出：

```
chetna agarwal

```

**参考**：
[http://php.net/manual/en/function.lcfirst.php](http://php.net/manual/en/function.lcfirst.php)