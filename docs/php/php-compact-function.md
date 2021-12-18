# PHP | compact()函数

> 原文:[https://www.geeksforgeeks.org/php-compact-function/](https://www.geeksforgeeks.org/php-compact-function/)

compact()函数是 PHP 中的内置函数，用于使用变量创建数组。该功能与[提取()功能](https://www.geeksforgeeks.org/php-extract-function/)相反。它创建一个关联数组，其键是变量名，对应的值是数组值。

**语法**:

```
*array* compact("variable 1", "variable 2"...)

```

**参数**:该函数接受由逗号运算符(“，”)分隔的可变数量的参数。这些参数是字符串数据类型，并指定我们要用来创建数组的变量的名称。我们还可以将一个数组作为参数传递给这个函数，在这种情况下，作为参数传递的数组中的所有元素都将被添加到输出数组中。

**返回值**:这个函数返回一个数组，数组中加入了所有的变量。

**注意**:任何作为参数传递的字符串，如果与有效变量名不匹配，将被跳过，不会被添加到数组中。

示例:

```
Input : $AS="ASSAM", $OR="ORISSA", $KR="KERELA"
        compact("AS", "OR", "KR");
Output :
Array
(
    [AS] => ASSAM
    [OR] => ORISSA
    [KR] => KERELA
)

```

下面的程序说明了 PHP 中 compact()函数的工作原理:

**示例-1** :

```
<?php
// PHP program to illustrate compact() 
// Function

$AS = "ASSAM";
$OR = "ORISSA";
$KR = "KERELA";

$stats = compact("AS", "OR", "KR");

print_r($states);

?>
```

输出:

```
Array
(
    [AS] => ASSAM
    [OR] => ORISSA
    [KR] => KERELA
)

```

**示例-2** :

```
<?php
// PHP program to illustrate compact() 
// function when an array is passed as
// a parameter

$username = "max";
$password = "many";
$age = "31";

$NAME = array("username", "password");

$result = compact($NAME, "age");

print_r($result);

?>
```

输出:

```
Array
(
    [username] => max
    [password] => many
    [age] => 31
)

```

**参考**:
T3】http://php.net/manual/en/function.compact.php