# PHP | array_diff_key()函数

> 原文:[https://www.geeksforgeeks.org/php-array_diff_key-function/](https://www.geeksforgeeks.org/php-array_diff_key-function/)

PHP 的这个内置函数用于获取一个或多个数组之间的差异。此函数比较一个或多个数组之间的键，并返回它们之间的差异。因此，该函数通常根据两个数组的键来比较它们，并返回第一个数组中存在但其他输入数组中不存在的元素。

**注意:**这个函数不同于 array_diff()和 array_diff_assoc()。第一个只使用值进行比较。第二种使用键和值进行比较。其中 as array_diff_key()只使用键进行比较。

**语法:**

```php
*array* array_diff_key($array1, $array2, $array3, ..., $array_n)
```

**参数:**函数可以取任意数量的数组作为需要比较的参数。

**返回类型:**此函数将第一个参数数组的键与其余数组进行比较，并返回一个数组，该数组包含$array1 中不存在于任何其他数组中的所有条目。

示例:

```php
Input : 
$array1 = ("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI", 
                      "40"=>"KISHAN", "50"=>"RISHI")
$array2 = ("10"=>"RAM", "70"=>"LAXMAN", "30"=>"KISHAN", 
                                        "80"=>"RAGHAV")
$array3 = ("30"=>"LAXMAN", "80"=>"RAGHAV")
Output :
Array
(
    [20] => LAXMAN
    [40] => KISHAN
    [50] => RISHI
)

Input :
$array1 = ("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI", 
                      "40"=>"KISHAN", "50"=>"RISHI");
$array2 = ("10"=>"LAXMAN", "40"=>"RAGHAV", "40"=>"KISHAN");
Output :
Array
(
    [10] => RAM
    [20] => LAXMAN
    [30] => RAVI
    [50] => RISHI
)

```

下面的程序说明了 PHP 中 array_diff_key()的工作原理:

```php
<?php

// PHP code to illustrate the 
// array_diff_key() function

// Input Arrays
$array1 = array("10"=>"RAM", "20"=>"LAXMAN", "30"=>"RAVI", 
                            "40"=>"KISHAN", "50"=>"RISHI");
$array2 = array("10"=>"RAM", "70"=>"LAXMAN", 
                "30"=>"KISHAN", "80"=>"RAGHAV");
$array3 = array("30"=>"LAXMAN", "80"=>"RAGHAV");

print_r(array_diff_key($array1, $array2, $array3));

?>
```

输出:

```php
Array
(
    [20] => LAXMAN
    [30] => RAVI
    [40] => KISHAN
    [50] => RISHI
)

```

**参考**:
T3】http://php.net/manual/en/function.array-diff-key.php