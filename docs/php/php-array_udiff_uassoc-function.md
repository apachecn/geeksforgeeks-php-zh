# PHP | array_udiff_uassoc()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ udiff _ UAS SOC-function/](https://www.geeksforgeeks.org/php-array_udiff_uassoc-function/)

array _ udiff _ uassoc()函数是 PHP 中的一个内置函数，用于区分两个或多个数组。该函数通过使用两个带有附加索引键的用户定义函数来计算差异数组。它通过使用回调函数来比较数据和索引，并返回差异。

**语法:**

```php
array_udiff_uassoc($arr1, $arr2, $arr3........nth array, value_Function, key_Function )
```

**使用的参数:**该 array_udiff_uassoc()函数参数描述如下:

1.  **$arr1、$arr2、$arr3、$arr4、…。，$arrn :** 这是我们想要区分的数组列表。
2.  **value_Function:** 此参数代表用户自定义函数。这个用户定义的函数将用于比较值。
3.  **key_Function:** 也是用户自定义的功能。这个用户定义的函数用于比较数组键。

**注意:**两个比较函数(value_Function、key_Function)如果第一个参数比第二个参数更为<、=、或>，则返回大于 0 的整数<、=、或>。

**返回值**:该函数返回一个数组，该数组包含所有其他数组中不存在的数组 *$arr1* 的值。

**一些相关功能:**

*   [**PHP | arr_diff()函数:**](https://www.geeksforgeeks.org/php-array_diff-function/) 计算一个数组的差。
*   [**PHP | arr_udiff()函数:**](https://www.geeksforgeeks.org/php-array_udiff-function/) 通过使用用户定义的回调函数计算数组的差异并比较数据。
*   [**PHP | array_diff_assoc()函数:**](https://www.geeksforgeeks.org/php-array_diff_assoc-function/) 用额外的索引键计算数组的差异。
*   [**PHP | array _ diff _ uasoc()函数:**](https://www.geeksforgeeks.org/php-array_diff_uassoc-function/) 该函数比较一个或多个数组之间的键和值，并返回第一个数组中不在其余数组中的元素。
*   [**PHP | array_diff_key()函数:**](https://www.geeksforgeeks.org/php-array_diff_key-function/) 将第一个参数数组的键与其余数组进行比较，并返回一个数组，该数组包含$array1 中不存在于任何其他数组中的所有条目。

下面的程序说明了数组函数。

**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to illustrate
// array_udiff_uassoc() function

// comparison function for array values
function value_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// comparison function for array keys
function key_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// array1  list for comparison.
$arr1 = array(
    "m" => "C lab",
    "n" => "Java lab",
    "o" => "C# lab",
    "x" => "C++ lab",
    "y" => "Ruby lab",
);

//array2  list for comparison.
$arr2 = array(
       "m" => "C lab",
    "b" => "Java lab",
    "c" => "C# lab",
    "x" => "C++ lab",
    "n" => "Ruby lab",
);

$result = array_udiff_uassoc($arr1,
    $arr2, "value_Function", "key_Function");

// print result.
print_r($result);
?>
```

**Output:** 

```php
Array
(
    [n] => Java lab
    [o] => C# lab
    [y] => Ruby lab
)
```

**程序:2**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to illustrate
// array_udiff_uassoc() function

// comparison function for array values
function value_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// comparison function for array keys
function key_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// array1  list for comparison.
$arr1 = array(
    "a" => "C lab",
    "b" => "Java lab",
    "c" => "C# lab",
    "d" => "C++ lab",
    "e" => "Ruby lab",
);

// array2  list for comparison.
$arr2 = array(
       "a" => "C lab",
    "b" => "Java lab",
    "c" => "C# lab",
    "d" => "C++ lab",
    "e" => "XML lab",
);
$arr3 = array(
    "a" => "C lab",
    "b" => "Java lab",
    "c" => "C# lab",
    "d" => "C++ lab",
    "e" => "CSS lab"
);
$arr4 = array(
    "a" => "C lab",
    "b" => "Java lab",
    "c" => "C# lab",
    "d" => "C++ lab",
    "e" => "PHP lab"
);

$result = array_udiff_uassoc($arr1, $arr2,
    $arr3, $arr4, "value_Function", "key_Function");

// print result.
print_r($result);
?>
```

**Output:** 

```php
Array
(
    [e] => Ruby lab
)
```

**程序:3**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to illustrate
// array_udiff_uassoc() function

// comparison function for array values
function value_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// comparison function for array keys
function key_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// array1  list for comparison.
$arr1 = array(
    "x" => "Geeks",
    "y" => "for",
    "z" => "Geeks",
);

// array2  list for comparison.
$arr2 = array(
     "x" => "Geeks",
    "y" => "for",
    "z" => "Geeks",
);

$result = array_udiff_uassoc($arr1,
    $arr2, "value_Function", "key_Function");

// print result.
print_r($result);
?>
```

**Output:** 

```php
Array
(
)
```

**程序:4** 取三个数组(array1 和 array2，array3)并使用比较函数 array_udiff_uassoc()函数。如果所有三个数组都有相同的索引，但值不同，则返回第一个数组。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to illustrate
// array_udiff_uassoc() function

// comparison function for array values
function value_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// comparison function for array keys
function key_Function($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// array1  list for comparison.
$arr1 = array(
    "a" => "C lab",
    "b" => "Java lab",
    "d" => "C# lab",
);

// array2  list for comparison.
$arr2 = array(
       "a" => "C ",
    "b" => "Java ",
    "d" => "C#",
);

// array3  list for comparison.
$arr3 = array(
    "a" => "Program",
    "b" => "Code",
    "d" => "Run",

);

$result = array_udiff_uassoc($arr1,
   $arr2, $arr3, "value_Function", "key_Function");

// print result.
print_r($result);
?>
```

**Output:** 

```php
Array
(
    [a] => C lab
    [b] => Java lab
    [d] => C# lab
)
```

**参考**:[http://php.net/manual/en/function.array-udiff-uassoc.php](http://php.net/manual/en/function.array-udiff-uassoc.php)T4】