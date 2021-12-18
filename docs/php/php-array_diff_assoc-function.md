# PHP | array_diff_assoc()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ diff _ assoc-function/](https://www.geeksforgeeks.org/php-array_diff_assoc-function/)

PHP 的这个内置函数用于获取一个或多个数组之间的差异。该函数比较一个或多个数组之间的键和值，并返回它们之间的差值。因此，该函数通常根据键和值比较两个数组，并返回第一个数组中存在但其他输入数组中不存在的元素。

**注意:**这个函数与 [PHP | array_diff()函数](https://www.geeksforgeeks.org/php-array_diff-function/)的不同之处在于后者只使用了值进行比较，但是在 array_diff_assoc()中我们同时使用了值和键进行比较。

**语法:**

```
array_diff_assoc($array1, $array2, $array3, ..., $arrayn)
```

**参数:**函数可以取任意数量的数组作为需要比较的参数。

**返回类型:**此函数将第一个参数数组的键和值与其余数组进行比较，并返回一个数组，该数组包含$array1 中不存在于任何其他数组中的所有条目。

示例:

```
Input : 
$array1 = ("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI", 
                        "40"=>"KISHAN", "50"=>"RISHI")
$array2 = ("10"=>"RAM", "70"=>"LAXMAN", "30"=>"KISHAN", 
                                          "80"=>"RAGHAV")
$array3 = ("20"=>"LAXMAN", "80"=>"RAGHAV")
Output :
Array
(
    [30] => RAVI
    [40] => KISHAN
    [50] => RISHI
)

Input :
$array1 = ("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI", 
                      "40"=>"KISHAN", "50"=>"RISHI")
$array2 = ("20"=>"LAXMAN", "40"=>"RAGHAV", "40"=>"KISHAN")
Output :
Array
(
    [10] => RAM
    [30] => RAVI
    [50] => RISHI
)

```

下面的程序说明了数组 _diff_assoc()在 PHP 中的工作原理:

```
<?php

// PHP code to illustrate the 
// array_diff_assoc() function

// Input Arrays
$array1 = array("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI",
                            "40"=>"KISHAN", "50"=>"RISHI");
$array2 = array("10"=>"RAM", "70"=>"LAXMAN", "30"=>"KISHAN",
                                            "80"=>"RAGHAV");
$array3 = array("20"=>"LAXMAN", "80"=>"RAGHAV");

print_r(array_diff_assoc($array1, $array2, $array3));

?>
```

输出:

```
Array
(
    [30] => RAVI
    [40] => KISHAN
    [50] => RISHI
)
```

**参考**:
T3】http://php.net/manual/en/function.array-diff-assoc.php