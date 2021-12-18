# PHP | array_sum()函数

> 原文:[https://www.geeksforgeeks.org/php-array_sum-function-2/](https://www.geeksforgeeks.org/php-array_sum-function-2/)

array_sum()函数返回数组中所有值的总和(一维和关联)。它接受一个数组参数，并返回其中所有值的总和。

```php
number array_sum ( $array )

```

**参数**
该函数唯一的参数是需要计算其和的数组。

**返回值**
该函数返回所有元素相加后的总和。返回的总和可以是整数或浮点数。如果数组为空，它也会返回 **0** 。

示例:

```php
Input : $a = array(12, 24, 36, 48);
        print_r(array_sum($a));
Output :120

Input : $a = array();
        print_r(array_sum($a));
Output :0

```

在第一个示例中，数组计算数组元素的总和并返回。在第二个例子中，返回的答案是 **0** ，因为数组是空的。

**程序–1**

```php
<?php
//array whose sum is to be calculated
$a = array(12, 24, 36, 48);

//calculating sum
print_r(array_sum($a));
?>
```

输出:

```php
120

```

**程序–2**

```php
<?php
//array whose sum is to be calculated
$a = array();

//calculating sum
print_r(array_sum($a));
?>
```

输出:

```php
0

```

**程序–3**

```php
<?php
// array whose sum is to be calculated
$b = array("anti" => 1.42, "biotic" => 12.3, "charisma" => 73.4);

// calculating sum
print_r(array_sum($b));
?>
```

输出:

```php
87.12

```

感谢 [HGaur](https://auth.geeksforgeeks.org/user/HGaur/articles) 提供以上例子。