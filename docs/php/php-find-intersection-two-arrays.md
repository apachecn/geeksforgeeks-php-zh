# PHP|查找两个数组的交集

> Original: [https://www.geeksforgeeks.org/php-find-intersection-two-arrays/](https://www.geeksforgeeks.org/php-find-intersection-two-arrays/)

您将获得两个 n 元素数组，每个数组包含 n 个元素。 您必须找到这两个元素的所有公共元素，而不使用 php 中的任何循环，并打印得到的公共元素数组。

示例：

```php
Input : array1[] = {3, 5, 2, 7, 9}, 
        array2[] = {4, 3, 2, 7, 8}
Output : array (
                [0] => 3,
                [1] => 2,
                [2] => 7)

Input : array1[] = {3, 5, 7}, 
        array2[] = {2, 4, 6}
Output : array (
                )

```

在[C](https://www.geeksforgeeks.org/c/)/[Java](https://www.geeksforgeeks.org/java/)中，我们必须遍历一个数组，并且对于每个元素，您必须检查它在第二个数组中是否存在。 但是 PHP 提供了一个内置函数(array_intersect())，它返回两个数组的公共元素(Intersect)。

**ARRAY_INTERSECT($array1，$array2)：**返回一个数组，其中包含 array2 中存在的 array1 的所有值。
*请注意，密钥是保留的。*

**注意：**由于 array_intersect()返回具有保留键的数组，因此我们将使用 array_values()，它将对键进行重新排序。

```php
// find intersect of both array
$result = array_intersect($array1, $array2);

// re-order keys
$result = array_values($result);

// print resultant array
print_r($result);

```

```php
<?php
// declare arrays
$array1 = array(2, 5, 7, 6, 9);
$array2 = array(3, 2, 5, 6, 8);

// find intersect of both array
$result = array_intersect($array1, $array2);

// re-order keys
$result = array_values($result);

// print resultant array
print_r($result);
?>
```

**Output:**

```php
Array
(
    [0] => 2
    [1] => 5
    [2] => 6
)

```