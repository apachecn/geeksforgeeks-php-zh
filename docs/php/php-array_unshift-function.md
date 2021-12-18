# PHP | array_unshift()函数

> 原文:[https://www.geeksforgeeks.org/php-array_unshift-function/](https://www.geeksforgeeks.org/php-array_unshift-function/)

PHP 的这个内置函数用于向数组中添加一个或多个元素，这些元素在数组的开头添加。我们添加到数组中的所有元素都以相同的顺序插入，就像它们已经被传递一样。它们从第 0 个位置开始进行数字索引。如果有字符串键，则它们保持不变。
**语法** :

```
*int* array_unshift($array, $val1, $val2, $val3....)
```

**参数:**
该函数可以取多个参数，具体取决于我们要插入数组的元素数量。我们基本上将参数分为两类，解释如下:

1.  **$array:** 这是一个强制参数，指的是我们要操作的原始数组。
2.  **List_of_values** :这是一组参数，代表我们需要插入到数组中的值列表， *$array* 。在上面的语法中，值列表是 *$val1，$val2，$val3。*。

**返回值:**该函数返回插入元素后新修改数组的元素总数。
示例:

```
Input : $array = ("ram", "krishna", "aakash")
        $val1 = "rohan", $val2 = "rajeeb", $val3 = "saniya"
Output :
Array
(
    [0] => rohan
    [1] => rajeeb
    [2] => saniya
    [3] => ram
    [4] => krishna
    [5] => aakash
)

Input : $array = (1=>"ram", 2=>"krishna", 3=>"aakash")
        $val1 = "rohan", $val2 = "rajeeb", $val3 = "saniya";
Output :
Array
(
    [0] => rohan
    [1] => rajeeb
    [2] => saniya
    [3] => ram
    [4] => krishna
    [5] => aakash
)
```

下面的程序说明了 PHP 中的 array_unshift()函数:

*   在这个程序中，我们将尝试通过在数组的开头添加元素来理解函数 array_unshift()的工作原理。我们还将观察到数字键是自动添加的。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate
// the use of array_unshift()

// Input Array
$array = array("ram", "krishna", "aakash");

// Values to be added
$a1 = "rohan";
$a2 = "rajeeb";
$a3 = "saniya";

// Calling array_unshift()
array_unshift($array, $a1, $a2, $a3);

// Print modified array
print_r($array);

?>
```

*   输出:

```
Array
(
    [0] => rohan
    [1] => rajeeb
    [2] => saniya
    [3] => ram
    [4] => krishna
    [5] => aakash
)
```

*   在上面的程序中，我们已经看到，如果一个非键数组被传递给 array_unshift()函数，那么它会被自动修改为带有数字键的数组。但是如果数组已经有了从零开始的数字键，那么在插入新元素之后，这些键将被修改。下面的程序说明了这一点:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate
// the use of array_unshift()

// Input Array
$array = array(1=>"ram", 2=>"krishna", 3=>"aakash");

// Values to be inserted
$a1 = "rohan";
$a2 = "rajeeb";
$a3 = "saniya";

// Calling array_unshift()
array_unshift($array, $a1, $a2, $a3);

// Print modified array
print_r($array);

?>
```

*   输出:

```
Array
(
    [0] => rohan
    [1] => rajeeb
    [2] => saniya
    [3] => ram
    [4] => krishna
    [5] => aakash
)
```

**参考**:
T3】http://php.net/manual/en/function.array-unshift.phpT5】