# PHP | array_diff_uassoc()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ diff _ UAS SOC-function/](https://www.geeksforgeeks.org/php-array_diff_uassoc-function/)

**array_diff_uassoc()** 函数是 PHP 中的内置函数，用于使用用户定义的函数比较键来获取一个或多个数组之间的差异。此函数将一个或多个数组之间的键和值进行比较，并返回第一个数组中不在其余数组中的元素。根据提供给该功能的用户定义功能来比较按键。

**注意:**这个函数不同于 [PHP | array_diff_assoc()函数](https://www.geeksforgeeks.org/php-array_diff_assoc-function/)因为在 array_diff_assoc()函数中，键是根据一些内部函数进行比较的，而在 array _ diff _ uassoc()函数中，键是根据作为参数传递给它的用户定义函数进行比较的。

**语法:**

```php
array_diff_uassoc($array1, $array2, $array3, ..., $arrayn, user_function)
```

**参数:**该函数接受数组列表作为参数，并接受用户定义的函数，该函数将用于键的比较。

1.  **list_of_array:** 这个函数取一个用空格分隔的数组列表，我们想从中找出区别。在上面的语法中，数组的列表是 *$array1，$array2，$array3，…，$ array yn*。该列表必须包含至少两个数组，否则将引发警告。
2.  **user_function:** 这是一个字符串类型参数，表示将用于键比较的用户定义函数的名称。如果第一个参数比第二个参数大**、小或等于**，则该函数返回一个小于、大于或等于 0 的整数**。**

**返回值:**该函数返回一个数组，该数组包含第一个数组 *$array1* 的元素，这些元素在参数中传递给它的其他数组中不存在。将第一个数组 *$array1* 的键和值与其余数组进行比较。键的比较是按照用户定义的函数进行的。

示例:

```php
Input : $a1=array(10=>"striver", 20=>"raj", 30=>"geek")
        $a2=array(20=>"striver", 10=>"raj", 30=>"geek")
        function user_function($a, $b)
        {
           if ($a===$b)
           {
              return 0;
           }
           return ($a>$b)?1:-1;
        }

Output: Array
        (
           [10] => striver
           [20] => raj
        )

Explanation:  Since user_function returns 0 when keys
are equal and 1 and -1 when greater and less respectively.
So, the elements with unequal keys are in the output array.

```

下面的程序说明了 PHP 中的 array_diff_uassoc()函数:

**程序 1** :

```php
<?php
// PHP program to illustrate the  
// array_diff_uassoc() function 

// user defined function that returns 0 if 
// $array1's keys are equal to any other 
// input array, else returns 1 if greater, 
// or -1 if smaller 
function user_function($a, $b)
{
  if ($a===$b)
  {
      return 0;
  }
  return ($a>$b)? 1: -1;
}

// Input Arrays
$a1=array(10=>"striver", 20=>"raj", 30=>"geek");
$a2=array(20=>"striver", 10=>"raj", 30=>"geek");

$result = array_diff_uassoc($a1, $a2, "user_function");

print_r($result);
?>
```

**输出:**

```php
Array
(
    [10] => striver
    [20] => raj
)

```

**程序 2** :

```php
<?php
// PHP program to illustrate the 
// array_diff_uassoc() function 

// user defined function that returns 1 if 
// $array1's keys are equal to any other 
// input array, else returns 1 if greater, 
// or 0 if smaller 
function user_function($a, $b)
{
  if ($a===$b)
  {
    return 1;
  }
  return ($a>$b)? 1: 0;
}

// Input Arrays
$a1 = array(10=>"striver", 20=>"raj", 30=>"geek");
$a2 = array(20=>"striver", 10=>"raj", 30=>"geek");

$result=array_diff_uassoc($a1, $a2, "user_function");
print_r($result);
?>
```

:
**输出:**

```php
Array
(
    [20] => raj
    [30] => geek
)

```

**参考**:
T3】http://php.net/manual/en/function.array-diff-uassoc.php