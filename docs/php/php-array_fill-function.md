# PHP | array_fill()函数

> 原文:[https://www.geeksforgeeks.org/php-array_fill-function/](https://www.geeksforgeeks.org/php-array_fill-function/)

array_fill()是 PHP 中的内置函数，用于用值填充数组。这个函数基本上创建了一个具有给定预填充值的用户定义数组。

**语法:**

```php
array_fill($start_index, $number_elements, $values)
```

**参数:**
array _ fill()函数采用三个参数，描述如下:

1.  **$start_index:** 此参数指定将值填充到数组中的开始位置，用户想要创建。如果$start_index 为负，则返回数组的第一个索引将是$start_index，以下索引将从零开始。所以最好给它赋一个正值。这是一个强制参数，必须提供。
2.  **$number_elements:** 这个参数是指元素的个数，用户想要输入到数组中。$number_elements 应为正数(对于版本 5.6.0，包括 0)，否则将引发 E_WARNING。这也是一个强制参数。
3.  **$values :** 这个参数是指我们要插入到数组中的值。这些值可以是任何类型。

**返回类型**:array _ fill()函数返回一个填充的用户自定义数组，其值由 *$value* 参数描述。

示例:

```php
Input : $start_index = 2; $number_elements = 3;
        $values = "Geeks";
Output :
        Array
        (
          [2] => Geeks
          [3] => Geeks
          [4] => Geeks
        )

Input : $start_index = -10; $number_elements = 3;
        $values = 45;
Output :
        Array
        (
          [-10] => 45
          [0] => 45
          [1] => 45
        )

```

下面的程序说明了 PHP 中 array_fill()函数的工作原理:

```php
<?php

// PHP code to illustrate the working of array_fill()

function Fill($start_index, $number_elements, $values){
    return(array_fill($start_index, $number_elements, $values));
}

// Driver Code
$start_index = 2;
$number_elements = 5;
$values = "Geeks";
print_r(Fill($start_index, $number_elements, $values));
?>
```

输出:

```php
Array
(
    [2] => Geeks
    [3] => Geeks
    [4] => Geeks
    [5] => Geeks
    [6] => Geeks
)

```

**参考**:[http://php.net/manual/en/function.array-fill.php](http://php.net/manual/en/function.array-fill.php)