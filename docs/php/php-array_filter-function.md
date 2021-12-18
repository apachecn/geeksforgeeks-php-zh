# PHP | array_filter()函数

> 原文:[https://www.geeksforgeeks.org/php-array_filter-function/](https://www.geeksforgeeks.org/php-array_filter-function/)

PHP 中的这个内置函数用于使用用户定义的函数(也称为回调函数)过滤数组的元素。array_filter()函数迭代数组中的每个值，将它们传递给用户定义的函数或回调函数。如果回调函数返回 true，则将数组的当前值返回到结果数组中，否则不返回。这样，数组的键得到保留，即原始数组和输出数组中元素的键是相同的。

**语法:**

```php
*array* array_filter($array, $callback_function, $flag)
```

**参数**:函数取三个参数，其中一个是必选的，另外两个是可选的。

1.  **$ array** (required): refers to the input array to be filtered.
2.  **$ callback _ function** (optional): refers to the user-defined function. If no function is provided, all entries equal to FALSE in the array will be deleted.
3.  **$ flag** (optional): refers to the parameter passed to the callback function.
    *   ARRAY _ FILTER _ USE _ KEY-–Pass the KEY as the only parameter to the callback function, not the value of the array.
    *   ARRAY _ FILTER _ USE _ BOth-–Pass values and keys as parameters to the callback instead of values.

**返回值**:该函数返回一个过滤后的数组。

下面是一个程序，展示了如何使用 array_filter()函数从数组中返回或过滤出偶数元素。

```php
<?php

// PHP function to check for even elements in an array
function Even($array)
{
    // returns if the input integer is even
    if($array%2==0)
       return TRUE;
    else 
       return FALSE; 
}

$array = array(12, 0, 0, 18, 27, 0, 46);
print_r(array_filter($array, "Even"));

?>
```

输出:

```php
Array
(
    [0] => 12
    [1] => 0
    [2] => 0
    [3] => 18
    [5] => 0
    [6] => 46
)

```

在这个例子中，我们将不传递回调函数，让我们看看输出。我们会看到没有打印 0 或假元素:

```php
<?php

// PHP function to check for even elements in an array
function Even($array)
{
    // returns if the input integer is even
    if($array%2==0)
       return TRUE;
    else 
       return FALSE; 
}

$array = array(12, 0, 0, 18, 27, 0, 46);
print_r(array_filter($array));

?>
```

输出:

```php
Array
(
    [0] => 12
    [3] => 18
    [4] => 27
    [6] => 46
)

```

**参考**:[http://php.net/manual/en/function.array-filter.php](http://php.net/manual/en/function.array-filter.php)