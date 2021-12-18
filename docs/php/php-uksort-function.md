# PHP|ukort()函数

> Original: [https://www.geeksforgeeks.org/php-uksort-function/](https://www.geeksforgeeks.org/php-uksort-function/)

*ukort()*函数是 PHP 中的内置函数，用于使用用户定义的比较函数根据键而不是值对数组进行排序。

**语法：**

```
*boolean* uksort($array, myFunction);

```

**参数：**此函数接受两个参数，说明如下：

1.  **$array**：此参数指定需要排序的数组。
2.  **myFunction**：此参数指定将用于对数组*$array*的键进行排序的用户定义函数的名称。 此比较函数必须返回整数。

**返回值：**此函数返回布尔值。 成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 ukort()函数：

**程序 1**：

```
<?php

// user-defined comparison function
function my_sort($x, $y)
{
    if ($x == $y) 
        return 0;

    return ($x > $y) ? -1 : 1;
}

// Input array
$names = array(
                "10" => "javascript",
                "20" => "php", 
                "60" => "vbscript",
                "40" => "jsp"
              );

uksort($names, "my_sort");

// printing sorted array
print_r ($names);
?>
```

产出：

```
Array
(
    [60] => vbscript
    [40] => jsp
    [20] => php
    [10] => javascript
)

```

**程序 2**：

```
<?php

// user-defined comparison function
function my_sort($x, $y)
{
    if ($x == $y) 
        return 0;

    return ($x > $y) ? 1 : -1;
}

// Input array
$names = array(
                "10" => "javascript",
                "20" => "php", 
                "60" => "vbscript",
                "40" => "jsp"
              );

uksort($names, "my_sort");

// printing sorted array
print_r ($names);
?>
```

产出：

```
Array
(
    [10] => javascript
    [20] => php
    [40] => jsp
    [60] => vbscript
)

```

**注**：如果根据用户定义的比较函数比较两个值相等，则它们在输出数组中的顺序将是未定义的。

**参考**：
[http://php.net/manual/en/function.uksort.php](http://php.net/manual/en/function.uksort.php)