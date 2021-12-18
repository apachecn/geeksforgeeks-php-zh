# PHP | array_keys()函数

> 原文:[https://www.geeksforgeeks.org/php-array_keys-function/](https://www.geeksforgeeks.org/php-array_keys-function/)

array_keys()是 PHP 中的内置函数，用于返回和数组的所有键或键的子集。

**语法:**

```php
*array* array_keys($input_array, $search_value, $strict)
```

**参数:**该函数取三个参数，其中一个是强制的，另外两个是可选的。

1.  **$ input _ array** (required): refers to the array we want to operate.
2.  **$ search _ value** (optional): refers to the array value of key elements that we want to search in the array. If this parameter is passed, the function will only return the key corresponding to this element, otherwise it will return all the keys of the array.
3.  **$ strict** (optional): determine whether strict comparison should be used when searching (= = =). The default value is false.

**返回值:**该函数根据传递的参数返回一个包含输入数组中所有键或键子集的数组。

示例:

```php
Input :  $input_array = ("one" => "shyam", 2 => "rishav", 
                                          "three" => "gaurav")         
Output :
Array
(
    [0] => one
    [1] => 2
    [2] => three
)

Input : $input_array = ("one", "two", "three", "one", 
                          "four", "three", "one", "one")
        $search_value = "one"
Output :
Array
(
    [0] => 0
    [1] => 3
    [2] => 6
    [3] => 7
)

```

在下面的程序中，我们将一个简单的关联数组传递给函数 array_keys()，以打印它的所有键:

```php
<?php

// PHP function to illustrate the use of array_keys()
function get_Key($array)
{
    $result = array_keys($array);
    return($result);
}

$array = array("one" => "shyam", 2 => "rishav", 
                             "three" => "gaurav");
print_r(get_Key($array));

?>
```

输出:

```php
Array
(
    [0] => one
    [1] => 2
    [2] => three
)

```

在下面的程序中，除了数组，我们还传递了一个只返回键位的值。

```php
<?php

// PHP function to illustrate the use of array_keys()
function get_Key($array, $search_value)
{
    $result = array_keys($array, $search_value);
    return($result);
}

$array = array("one", "two", "three", "one", "four", 
                               "three", "one", "one");
$search_value = "one";
print_r(get_Key($array, $search_value));

?>
```

输出:

```php
Array
(
    [0] => 0
    [1] => 3
    [2] => 6
    [3] => 7
)

```

**参考**:[http://php.net/manual/en/function.array-keys.php](http://php.net/manual/en/function.array-keys.php)