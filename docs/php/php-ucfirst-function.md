# PHP|ucfirst()函数

> Original: [https://www.geeksforgeeks.org/php-ucfirst-function/](https://www.geeksforgeeks.org/php-ucfirst-function/)

**ucfirst()**函数是 PHP 中的一个内置函数，它接受一个字符串作为参数，并返回第一个字符为大写的字符串，而所有其他字符保持不变。

**语法：**

```
ucfirst($string)
```

**参数：**该函数只接受一个必选参数*$string*。 此参数表示其第一个字符将更改为大写的字符串。

**返回值：**该函数仅通过将传递的参数*$string 的第一个字符更改为大写来返回相同的字符串。*

例如：

```
Input : "geeks for geeks"
Output : Geeks for geeks

Input : "Chetna Agarwal"
Output : Chetna Agarwal

```

下面的程序演示了 PHP 中的 ucfirst()函数：

**程序 1：**下面的程序演示了 ucfirst()函数的用法。

```
<?php
    // PHP program that demonstrates the 
    // use of ucfirst() function 

    $str = "geeks for geeks";

    // converts the first case to upper case 
    // and prints the string
    echo(ucfirst($str)); 
?>
```

发帖主题：Re：Колибри0.7.0

```
Geeks for geeks

```

**程序 2：**下面的程序演示了起始字符为大写时 ucfirst()函数的用法。

```
<?php
    // PHP program that demonstrates the 
    // use of ucfirst() function when 
    // the first case is already in uppercase

    $str = "Chetna Agarwal";

    // already the first character is in upper case 
    // so prints the same string only
    echo(ucfirst($str)); 
?>
```

发帖主题：Re：Колибри0.7.0

```
Chetna Agarwal

```

**参考**：
[http://php.net/manual/en/function.ucfirst.php](http://php.net/manual/en/function.ucfirst.php)