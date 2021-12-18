# PHP | array _ uiintersection _ assoc()函数

> 原文:[https://www . geeksforgeeks . org/PHP-array _ uiintersect _ assoc-function/](https://www.geeksforgeeks.org/php-array_uintersect_assoc-function/)

**array _ uiintersection _ assoc()函数**是 PHP 中的一个内置函数，用于计算两个或多个数组的不同值的键数组的交集。初始数组或第一个数组通过回调函数或用户定义函数与所有其他数组进行比较，并返回匹配项。不同于[array _ uiintersection()](https://www.geeksforgeeks.org/php-array_uintersect-function/)函数，这些键用于比较。

**语法:**

```php
*array* array_uintersect_assoc( $array1, $array2, $array3... array nth, arr_uintersect_Function)
```

**参数:**该功能接受许多参数，如上所述，如下所述:

*   **$array1:** 是与另一个数组比较的初始数组。它是强制参数。
*   **$array2:** 是与第一个数组键相比的第二个数组。它也是强制参数。
*   **$array3…:** 与第一个数组键比较的数组。它是可选参数。
*   **arr _ uiintersection _ Function:**必选参数，用于保存用户自定义函数。它是定义用户定义的回调函数的字符串，如果第一个参数小于、等于或大于第二个参数，则返回小于、等于或大于零的整数。

**返回值:**它返回一个数组类型值，该值包含所有其他数组中存在的第一个数组。如果没有匹配项，则返回空值。

**注意:**array _ uiintersection _ assoc()函数比较数组的键，用户自定义函数比较值。

**示例:**

```php
Input :
    $arr1 = array( "a"=>"Website", "b"=>"frontend", "c"=>"programmer" );
    $arr2 = array( "a"=>"Website", "b"=>"backend ", "c"=>"programmer" );
    $arr3 = array( "a"=>"Website", "b"=>"fullstack ", "c"=>"programmer" );
    $arr4 = array( "a"=>"Website", "b"=>"maintenance ", "c"=>"Team" );
Output :
    Array (
        [a] => Website
    )
Explanation: Only one element (website) is common in all arrays.

Input :
    $arr1 = array( "a"=>"Software", "b"=>"Testing", "c"=>"Tool" );
    $arr2 = array( "a"=>"Software", "b"=>"Testing ", "c"=>"Team" );
Output :
    Array (
        [a] => Software
        [b] => Testing
)
Explanation: Two values are common in both array = Software, and Testing.
```

下面的程序说明了 PHP 中的 array _ uintersect _ assoc()函数:

**程序 1:** 该程序使用两个数组(array1 和 array2)和一个用户自定义的键比较函数(arr _ uintersect _ Function)。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program for array_uintersect_assoc() function
function arr_uintersect_Function($a, $b) {
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// Two array list with index and values
$arr1 = array (
    "a" => "Java",
    "b" => "Program",
    "c" => "Practice",
    "d" => "in",
    "f" => "Geeksforgeeks"
);
$arr2 = array (
    "a" => "Java",
    "b" => "Code ",
    "c" => "write",
    "d" => "in",
    "f" => "GeeksforgeeksIDE"
);

$result = array_uintersect_assoc($arr1, $arr2, "arr_uintersect_Function");

// Display result
print_r($result);

?>
```

**Output:** 

```php
Array
(
    [a] => Java
    [d] => in
)
```

**程序 2:** 该程序使用两个数组(array1 和 array2)和一个用户自定义的键比较函数(arr _ uintersect _ Function)。如果数组不匹配任何键和值，则返回空值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program for array_uintersect_assoc() function

// User-defined function
function arr_uintersect_Function($a, $b) {
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

// Two array list with index and values
$arr1 = array (
    "a" => "my",
    "b" => "best",
    "c" => "programming",
    "d" => "blog",
    "e" => "Geeksforgeeks"
);
$arr2 = array (
    "f" => "My",
    "g" => "first ",
    "h" => "program",
    "i" => "Geeks Hello"
);
$arr3 = array (
    "j" => "Analysis",
    "k" => "Algorithm ",
    "l" => "and",
    "m" => "Practice"
);

$result = array_uintersect_assoc( $arr1, $arr2, $arr3, "arr_uintersect_Function" );

// Display result
print_r($result);

?>
```

**Output:** 

```php
Array
(
)
```

**程序 3:** 该程序返回所有参数中存在的$arr1 的所有值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$arr1 = array (
    "a" => "gfg",
    "b" => "ide",
    "c" => "runcode"
);
$arr2 = array (
    "a" => "GFG",
    "B" => "practice"
);
$arr3 = array (
    "a" => "Gfg",
    "B" => "contribute"
);

print_r( array_uintersect_assoc($arr1, $arr2, $arr3, "strcasecmp") );

?>
```

**Output:** 

```php
Array
(
    [a] => gfg
)
```

**参考:**T2T4】