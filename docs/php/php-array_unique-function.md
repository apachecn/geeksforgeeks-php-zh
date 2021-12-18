# PHP | array_unique()函数

> 原文:[https://www.geeksforgeeks.org/php-array_unique-function/](https://www.geeksforgeeks.org/php-array_unique-function/)

很多时候，在编写程序或开发时，我们需要过滤数组来删除重复项。PHP 为我们提供了一个内置的函数来做到这一点，让事情变得简单。array_unique()是 PHP 中的内置函数，该函数从数组中移除重复的值。如果数组中有多个元素具有相同的值，则第一个出现的元素将被保留，该元素的所有其他出现将从数组中删除。

此外，根据该函数，当且仅当(字符串)$elem1 ==(字符串)$elem2 时，即当元素的字符串表示相同时，两个元素被视为相等。

**语法**:

```php
*array* array_unique($array , $sort_flags)

```

**注**:数组的键保留。也就是说，输入数组中未移除元素的键在输出数组中是相同的。

**参数**:该功能接受两个参数，其中一个是强制的，另一个是可选的。这两个参数描述如下:

1.  **$array** :此参数是必须提供的，它指定了我们要从中删除重复项的输入数组。
2.  **$sort_flags** :此为可选参数。此参数$sort_flags 可用于使用以下值修改排序行为:
    *   这是参数$sort_flags 的默认值。该值告诉函数正常比较项目(不要改变类型)。
    *   SORT_NUMERIC:这个值告诉函数用数字比较项目。
    *   这个值告诉函数将项目作为字符串进行比较。
    *   SORT_LOCALE_STRING:该值告诉函数根据当前的区域设置将项目作为字符串进行比较。

**返回值**:array _ unique()函数从数组中移除所有重复项后，返回过滤后的数组。

下面的程序说明了 PHP 中的 array_unique()函数:

**示例-1** :

```php
<?php

// Input Array
$a=array("red", "green", "red", "blue");

// Array after removing duplicates
print_r(array_unique($a));

?>
```

输出:

```php
Array
(
    [0] => red
    [1] => green
    [3] => blue
)
```

**示例-2** :

```php
<?php

// Input array
$arr = array("a"=>"MH", "b"=>"JK", "c"=>"JK", "d"=>"OR");

// Array after removing duplicates
print_r(array_unique($arr));

?>
```

输出:

```php
Array
(
    [a] => MH
    [b] => JK
    [d] => OR
)

```

**需要注意的要点:**

*   array_unique()不适用于多维数组。
*   输入数组的键被保留。
*   根据这个函数，如果两个元素的字符串表示相同，则认为它们相等。

**参考**:
[http://PHP . net/manual/en/function . array-unique . PHP](http://php.net/manual/en/function.array-unique.php)