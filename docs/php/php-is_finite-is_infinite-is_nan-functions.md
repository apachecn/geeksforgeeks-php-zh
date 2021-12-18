# PHP|IS_FINITED()、IS_INFINITE()、IS_NaN()函数

> Original: [https://www.geeksforgeeks.org/php-is_finite-is_infinite-is_nan-functions/](https://www.geeksforgeeks.org/php-is_finite-is_infinite-is_nan-functions/)

给定任何数值，它可以分为有限数、无限数和非数或俗称 NaN 三种不同的类型。 在开发高度依赖用户输入的项目时，可能会出现许多情况，其中用户提供了不适当的输入，而函数需要有限的数字输入，从而造成未处理的情况或意外的结果。

因此，检查给定的输入值是否有限是一种安全的选择。

**is_finite()函数**

**语法：**

```
*bool* is_finite ($value)

```

**参数**：该函数接受单个参数，该参数是要检查的浮点数。

**返回类型**：如果给定值有限，则此函数返回 TRUE，否则返回 FALSE。

例如：

```
Input :  $value = M_PI_4;
Output : TRUE

Input : $value = log(0);
Output : FALSE        

```

**IS_INFINITE()函数**

**语法：**

```
*bool* is_infinite ($value)

```

**参数**：该函数接受单个参数，该参数是要检查的浮点数。

**返回类型**：如果给定值为无穷大，则此函数返回 TRUE，否则返回 FALSE。

例如：

```
Input :  $value = M_PI_4;
Output : FALSE

Input : $value = log(0);
Output : TRUE        

```

**is_nan()函数**

**语法：**

```
*bool* is_nan ($value)

```

**参数**：该函数接受单个参数，该参数是要检查的浮点数。

**返回类型**：如果给定值不是数字，则此函数返回 TRUE，否则返回 FALSE。

例如：

```
Input :  $value = M_PI_4;
Output : FALSE

Input : $value = acos(1.1); // cos function can not be greater than 1
Output : TRUE        

```

下面的程序演示了 PHP 中 is_Finite()、is_INFINITE()、IS_NaN()函数的工作原理：

```
<?php

// PHP code to illustrate the working of 
// is_finite(), is_infinte() and is_nan() Functions 

// Finite Value: PI
$val1 = M_PI; 
// In-built value of INFINITY
$val2 = INF; 
// Produces NaN as COS value can reside 
// between -1 to +1 both inclusive
$val3 = acos(-1.01); 

echo var_dump(is_finite($val1), is_finite($val2), 
                            is_finite($val3))."\n";
echo var_dump(is_infinite($val1), is_infinite($val2), 
                          is_infinite($val3))."\n";
echo var_dump(is_nan($val1), is_nan($val2), 
                        is_nan($val3))."\n";

?>
```

产出：

```
bool(true) bool(false) bool(false) 
bool(false) bool(true) bool(false) 
bool(false) bool(false) bool(true) 

```

**需要注意的重要事项**：

*   此函数还可以检查表达式是否产生有限结果，但如果表达式导致 NaN PHP 本身显示错误，则返回默认 FALSE，例如检查除以零表达式的情况。
*   IS_FINITED()函数在许多项目中都被使用，以使其更加安全和高效。
*   这些方法可以产生非常精确的结果，但是时间效率不高。