# PHP | array _ uiintersection _ UAS SOC()函数

> 原文:[https://www . geeksforgeeks . org/PHP-array _ uiintersect _ UAS SOC-function/](https://www.geeksforgeeks.org/php-array_uintersect_uassoc-function/)

array _ uintersect _ uassoc()函数是 PHP 中的一个内置函数，用于计算两个数组的交集。回调函数的作用是帮助比较和计算索引值，它比较键。它还使用两个用户定义的函数比较两个或多个数组中的值，然后返回匹配项。array _ uintersect _ uassoc()返回一个包含所有参数中第一个数组的所有值的数组。为了进行比较，在第一个函数中使用键，在第二个函数中使用该值。

**语法:**

```
array array_uintersect_uassoc( $array1, $array2, $array3..., $function_key, $function_value )
```

**参数:**该函数接受多个参数，如上所述，如下所述:

*   **Array 1:** This is the first array, which is mandatory and used for comparison with other arrays.
*   **Array 2:** This is the forced second array, which is used to compare with the first array and other arrays.
*   **Array3 and other arrays:** is an optional parameter. This is an array for comparison with other arrays.
*   **Function key:** is the required parameter. It is the name of the user-defined function that compares array keys.
*   **Function value:** is a required parameter. It is the name of the user-defined function that compares array values.

**返回值:**它返回一个数组，该数组包含所有参数中存在的数组 1 的所有值。

下面的程序说明了 PHP 中的数组函数:

**节目 1:**

```
<?php
$arr1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$arr2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_uassoc($arr1, $arr2, "strcasecmp", "strcasecmp"));
?>
```

**输出:**

```
Array
(
    [a] => green
    [b] => brown
)

```

**节目 2:**

```
<?php
function function_key($a, $b)
{
    if ($a == $b)
        return 0;

    return ($a > $b) ? 1 : -1;
}

function function_value($a, $b)
{
    if ($a == $b)
        return 0;

    return ($a > $b) ? 1 : -1;
}

$arr1=array("1"=>"Geeks","2"=>"GeeksforGeeks","3"=>"Geeks1");
$arr2=array("1"=>"Geeks","2"=>"GFG","3"=>"Geeks1");

$res = array_uintersect_uassoc($arr1, $arr2, "function_key", "function_value");

print_r($res);
?>
```

**输出:**

```
Array 
( 
    [1] => Geeks 
    [3] => Geeks1 
)

```

**参考:**[http://PHP . net/manual/en/function . array-uiintersection-UAS SOC . PHP](http://php.net/manual/en/function.array-uintersect-uassoc.php)