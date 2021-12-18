# PHP|usort()函数

> Original: [https://www.geeksforgeeks.org/php-usort-function/](https://www.geeksforgeeks.org/php-usort-function/)

PHP 附带了许多内置函数，用于以更简单的方式对数组进行排序。 这里，我们将讨论一个新函数 usort()。 PHP 中的 usort()函数使用用户定义的比较函数对给定的数组进行排序。 如果我们想要以一种新的方式对数组进行排序，则此函数非常有用。 此函数将从零开始的新整数键分配给数组中存在的元素，旧键将丢失。

**语法：**

```php
*boolean* usort( $array, "function_name");

```

**参数：**此函数接受上述语法中所示的两个参数，如下所示：

1.  **$array**：此参数指定要排序的数组。
2.  **Function_Name**：此参数指定用户定义函数的名称，该函数用于比较值并对参数*$array*指定的数组进行排序。 此函数根据以下条件返回整数值。 如果两个参数相等，则返回 0；如果第一个参数大于第二个参数，则返回 1；如果第一个参数小于第二个参数，则返回-1。

**返回值：**此函数返回值的布尔类型。 成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 usort()函数：

```php
<?php

    // PHP program to illustrate usort() function

    // This is the user-defined function used to compare
    // values to sort the input array
    function comparatorFunc( $x, $y)
    {   
        // If $x is equal to $y it returns 0
        if ($x== $y)
            return 0;

        // if x is less than y then it returns -1
        // else it returns 1    
        if ($x < $y)
            return -1;
        else
            return 1;
    }

    // Input array
    $arr= array(2, 9, 1, 3, 5); 

    usort($arr, "comparatorFunc");

    print_r($arr);

?>
```

产出：

```php
Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 5
    [4] => 9
)

```

**参考**：
[http://php.net/manual/en/function.usort.php](http://php.net/manual/en/function.usort.php)