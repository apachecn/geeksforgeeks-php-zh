# PHP 将一个数组附加到另一个数组

> 原文:[https://www . geesforgeks . org/PHP-append-一个数组到另一个数组/](https://www.geeksforgeeks.org/php-append-one-array-to-another/)

给定两个数组 *arr1* 和 *arr2* ，任务是将一个数组追加到另一个数组中。

示例:

```php
Input : arr1 = [ 1, 2 ]
        arr2 = [ 3, 4 ]

Output : arr1 = [ 1, 2, 3, 4 ]

Input : arr1 = [ "Geeks", "g4g" ]
        arr2 = [ "GeeksforGeeks" ]

Output : arr1 = [ "Geeks", "g4g", "GeeksforGeeks" ]

```

**使用 array_merge 函数:**该函数在合并两个数组后返回一个新的数组。

**例:**

```php
<?php
$arr1 = array("Geeks", "g4g");
$arr2 = array("GeeksforGeeks", "Computer science portal");

// Get the merged array in the first array itself.
$arr1 = array_merge($arr1, $arr2); 

echo "arr1 Contents:";

// Use for each loop to print all the array elements.
foreach ($arr1 as $value) {
    echo $value . "\n";
}
?>
```

**输出:**

```php
arr1 Contents:
Geeks
g4g
GeeksforGeeks
Computer science portal
```

**使用 array_push 方法:**此方法就地推送第一个数组中的第二个数组元素。

**例:**

```php
<?php
$arr1 = array(1, 2);
$arr2 = array(3, 4);

// arr2 elements are being pushed in the arr1.
array_push($arr1 , ...$arr2); 

echo "arr1 = ";

// Use for each loop to print all the array elements.
foreach ($arr1 as $value) {
echo $value . ' ';
}
?>
```

**输出:**

```php
arr1 = 1 2 3 4
```

**注意:**另一种方法是用“+”号，但在较新的版本中会给出致命警告，因此不推荐使用。