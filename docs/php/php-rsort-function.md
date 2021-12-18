# PHP|rort()函数

> Original: [https://www.geeksforgeeks.org/php-rsort-function/](https://www.geeksforgeeks.org/php-rsort-function/)

**rort()**是 PHP 中的一个内置函数，用于按**降序**(即从大到小)对数组进行排序。 它对实际数组进行排序，因此更改会反映在数组本身中。 该函数为我们提供了 6 种排序类型，可以根据这些类型对数组进行排序。

**语法：**

```php
rsort($array, sorting_type)

```

**参数：**

1.  **$array**：该参数指定要排序的数组。
2.  **SOLING_TYPE**：可选参数。 此参数指定将在输入数组上执行排序操作的模式。 有 6 种分类类型，如下所述：
    *   **SORT_Regular**-当我们在**SORT_TYPE**参数中传递**0**或**SORT_Regular**时，将正常比较数组中的项
    *   **SORT_NUMERIC**-当我们在**SORT_TYPE**参数中传递**1**或**SORT_NUMERIC**时，将对数组中的项进行数值比较
    *   **SORT_STRING**-当我们在**SORT_TYPE**参数中传递**2**或**SORT_STRING**时，将按字符串比较数组中的项
    *   **SORT_LOCALE_STRING**-当我们在**SORT_TYPE**参数中传递**3**或**SORT_LOCALE_STRING**时，数组中的项将根据当前区域设置作为字符串进行比较
    *   **SORT_NATUAL**-当我们在**SORT_TYPE**参数中传递**4**或**SORT_Natural**时，数组中的项将使用自然排序作为字符串进行比较
    *   **SORT_FLAG_CASE**-当我们在**SORT_TYPE**参数中传递**5**或**SORT_FLAG_CASE**时，数组中的项目将作为字符串进行比较。 这些项目被视为不区分大小写，然后进行比较。 它可以与**SORT_Natural**或**SORT_STRING**一起使用|(按位运算符)。

**返回值：**返回布尔值，成功返回 TRUE，失败返回 FALSE。 它按降序对原始数组进行排序，该数组将作为参数传递给它。

**示例：**

```php
Input : $array = [3, 4, 1, 2] 
Output : 
Array
(
    [0] => 4
    [1] => 3
    [2] => 2
    [3] => 1
)

Input : $array = ["geeks2", "raj1", "striver3", "coding4"]
Output :
Array
(
    [0] => striver3 
    [1] => raj1 
    [2] => geeks2 
    [3] => coding4
)

```

下面的程序演示了 PHP 中的 rort()函数：

**程序 1：**按降序演示 rort()函数用法的程序。

## PHP

```php
<?php
// PHP program to demonstrate the use of rsort() function

$array = array(3, 4, 2, 1);

// sorting function used
rsort($array);

//prints the sorted array
print_r($array);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => 4
    [1] => 3
    [2] => 2
    [3] => 1
)

```

**程序 2：**演示如何使用 rort()函数以大小写敏感的降序对字符串进行排序的程序。

## PHP

```php
<?php
// PHP program to demonstrate the use of rsort() function
// sorts the string case-sensitively
$array = array("geeks", "Raj", "striver", "coding", "RAj");

// sorting function used, sorts the string case-sensitively
rsort($array, SORT_STRING);

// prints the sorted array
print_r($array);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => striver
    [1] => Raj
    [2] => RAj
    [3] => geeks
    [4] => coding
)

```

**程序 3：**演示如何使用 rort()函数以不区分大小写的降序对字符串进行排序的程序。

## PHP

```php
<?php
// PHP program to demonstrate the use of rsort() function
// sorts the string case-insensitively
$array = array("geeks", "Raj", "striver", "coding", "RAj");

// sorting function used, sorts the
// string case-insensitively
rsort($array, SORT_STRING | SORT_FLAG_CASE);

// prints the sorted array
print_r($array);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => striver
    [1] => Raj
    [2] => RAj
    [3] => geeks
    [4] => coding
)

```

**参考**：
[http://php.net/manual/en/function.rsort.php](http://php.net/manual/en/function.rsort.php)