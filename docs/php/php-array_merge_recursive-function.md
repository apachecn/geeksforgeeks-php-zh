# PHP | array_merge_recursive()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ merge _ recursive-function/](https://www.geeksforgeeks.org/php-array_merge_recursive-function/)

**array_merge_recursive()** 是 PHP 中的一个内置函数，用于递归地将两个或多个数组合并成一个数组。该函数用于将两个或多个数组的元素或值合并成一个数组。合并的方式是将一个数组的值附加在前一个数组的末尾。如果给定数组中有相同的键，则给该键分配一个值，该值的数组由具有相同键的值组成。

**注意:**该函数与 [array_merge()](https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/) 的不同之处在于，对于具有相同键的多个数组，array_merge()函数从所有数组中取最后一个数组值，但是在 **array_merge_recursive()** 中，键被分配了一个数组，该数组由具有相同键的数组的所有值组成。

**语法:**

```
array_merge_recursive($array1, $array2, $array3...$arrayn)
```

**参数:**函数可以取任意数量的数组作为参数，用逗号(，)分隔，我们需要合并。第一个参数 *$array1* 是强制的。

**返回值:**该函数返回一个合并数组，该数组合并了所有数组。合并的方式是将一个数组的值附加在前一个数组的末尾。如果给定数组中有相同的键，则输出数组中的该键被分配一个由具有相同键的值组成的数组。

示例:

```
Input : $a1=array("a"=>"raj", "b"=>"striver");
        $a2=array("z"=>"geeks", "b"=>"articles");
Output : 
Array
(
    [a] => raj
    [b] => Array
        (
            [0] => striver
            [1] => articles
        )

    [z] => geeks
)
Explanation: "striver" and "articles" has the same 
key "b", so the key b is assigned to an array which has 
"striver" and "articles" as elements. 

Input :$a1=array("a"=>"raj", "b"=>"striver");
       $a2=array("z"=>"geeks", "d"=>"articles");
Output :
Array
(
    [a] => raj
    [b] => striver
    [z] => geeks
    [d] => articles
)

```

下面的程序说明了 array_merge_recursive()函数:

**程序 1:** 用所有不同的键演示 array_merge_recursive()
函数的 PHP 程序。

```
<?php
// PHP program to demonstrate array_merge_recursive() 
// function with same keys
$a1=array("a"=>"raj", "b"=>"striver");
$a2=array("z"=>"geeks", "d"=>"articles");

print_r(array_merge_recursive($a1, $a2));
?>
```

输出:

```
Array
(
    [a] => raj
    [b] => striver
    [z] => geeks
    [d] => articles
)

```

**程序二:**用相同的键演示 array_merge_recursive()函数的 PHP 程序。

```
<?php
// PHP program to demonstrate array_merge_recursive() 
// function with same keys
$a1=array("a"=>"raj", "b"=>"striver");
$a2=array("z"=>"geeks", "b"=>"articles");

//function call
print_r(array_merge_recursive($a1, $a2));
?>
```

输出:

```
Array
(
    [a] => raj
    [b] => Array
        (
            [0] => striver
            [1] => articles
        )

    [z] => geeks
)

```

**参考**:
T3】http://php.net/manual/en/function.array-merge-recursive.php