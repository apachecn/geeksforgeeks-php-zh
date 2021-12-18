# PHP|List()函数

> Original: [https://www.geeksforgeeks.org/php-list-function/](https://www.geeksforgeeks.org/php-list-function/)

**list()**函数是 PHP 中的一个内置函数，用于一次将数组值赋给多个变量。 此函数仅适用于[数值数组。](https://www.geeksforgeeks.org/php-arrays/) 当数组被赋以多个值时，数组中的第一个元素被赋值给第一个变量，第二个元素被赋值给第二个变量，依此类推，直到变量数满为止。 变量数不能超过数值数组的长度。

**语法：**

```
list($variable1, $variable2....)
```

**参数：**它接受由空格分隔的变量列表。 这些变量被赋值。 必须至少将一个变量传递给函数。

**返回值：**函数向传递的多个变量返回赋值的数组。 如果传递的变量数大于数组中的元素数，则会引发错误。

下面的程序演示了 PHP 中的 list()函数：

**程序 1：**演示 list()函数用法的程序。

```
<?php

// PHP program to demonstrate the 
// use of list() function 
$array = array(1, 2, 3, 4);

// Assign array values to variables 
list($a, $b, $c) = $array; 

// print all assigned values 
echo "a =", ($a), "\n";
echo " b =", ($b), "\n";
echo " c =", ($c), "\n"; 

// Perform multiplication of
// those assigned numbers
echo "a*b*c =", ($a*$b*$c); 

?>
```

发帖主题：Re：Колибри0.7.0

```
 a =1
 b =2
 c =3
a*b*c =6
```

**程序 2：**演示 list()函数运行时错误的程序。

```
<?php

// PHP program to demonstrate the 
// runtime error of list() function 
$array = array(1, 2, 3, 4);

// assign array values to variables 
list($a, $b, $c, $d, $e) = $array; 

?>
```

发帖主题：Re：Колибри0.7.0

```
PHP Notice:  Undefined offset: 4 in 
/home/619f1441636b952bbd400f1e9e8e3d0c.php on line 6

```

**程序 3：**演示将数组中的特定索引值赋给变量的程序。

```
<?php

// PHP program to demonstrate assignment of 
// particular index values in the array to 
// variables. 
$array = array(1, 2, 3, 4);

// Assign array values to variables 
list(, , $a) = $array; 

// Print all assigned values 
echo " a = ", ($a), "\n";  

?>
```

发帖主题：Re：Колибри0.7.0

```
a = 3

```

**参考**：
[http://php.net/manual/en/function.list.php](http://php.net/manual/en/function.list.php)