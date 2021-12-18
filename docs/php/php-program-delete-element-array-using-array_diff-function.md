# PHP|使用 array_diff()

从数组中删除元素

> Original: [https://www.geeksforgeeks.org/php-program-delete-element-array-using-array_diff-function/](https://www.geeksforgeeks.org/php-program-delete-element-array-using-array_diff-function/)

给定一个数组，我们必须使用 PHP 中的 array_diff()函数从该数组中删除一个元素。

例如：

```php
Input : $arr = array(2, 8, 9, 7, 6, 5);
        $arr = array_diff($arr, array(9));
Output : Array
         (
             [0] => 2
             [1] => 8
             [3] => 7
             [4] => 6
             [5] => 5
         )

Input : $arr = array("shubham", "akshay", "vishal", "sweta");
        $arr = array_diff($arr, array("akshay"));
Output : Array
         (
             [0] => shubham
             [2] => vishal
             [3] => sweta
         )

```

**[array_diff()](https://contribute.geeksforgeeks.org/microsoft-office-india-interview-experience-set-170-2-years-exp/)**array_diff()函数接受两个或多个参数，并返回包含第一个数组中其他数组中不存在的值的数组。

**方法**：解决这个问题的想法是将两个数组作为参数传递给 array_diff()函数。 参数中的第一个数组将是我们要从中删除元素的数组。 第二个数组将包含我们要从第一个数组中删除的单个元素。 最后，我们将把 array_diff()函数返回的结果数组存储在输入数组中。

以下程序说明了上述方法：

**程序 1：**

```php
<?php

    $arr = array(2, 8, 9, 7, 6, 5);

    // returns the array after removing
    // the array value 9
    $arr = array_diff($arr, array(9));

    print_r ($arr);

?>
```

产出：

```php
Array
(
    [0] => 2
    [1] => 8
    [3] => 7
    [4] => 6
    [5] => 5
)

```

**程序 2：**

```php
<?php

    $arr = array("Harsh", "Nishant", "Akshay", 
                                "Barun", "Bikash");

    // returns the array after removing
    // the array value "Akshay"
    $arr = array_diff($arr, array("Akshay"));

    print_r ($arr);

?>
```

产出：

```php
Array
(
    [0] => Harsh
    [1] => Nishant
    [3] => Barun
    [4] => Bikash
)

```