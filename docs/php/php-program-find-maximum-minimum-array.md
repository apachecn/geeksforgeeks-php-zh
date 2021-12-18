# 在数组

中查找最大值和最小值的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-find-maximum-minimum-array/](https://www.geeksforgeeks.org/php-program-find-maximum-minimum-array/)

给定一个整数数组，找出其中的最大值和最小值。
示例：

```php
Input : arr[] = {2, 3, 1, 6, 7}
Output : Maximum integer of the given array:7
         Minimum integer of the given array:1

Input  : arr[] = {1, 2, 3, 4, 5}
Output : Maximum integer of the given array : 5
         Minimum integer of the given array : 1
```

**方法 1(简单)：**我们简单地遍历数组，找出它的最大值和最小值。

## PHP

```php
<?php
// Returns maximum in array
function getMax($array)
{
   $n = count($array);
   $max = $array[0];
   for ($i = 1; $i < $n; $i++)
       if ($max < $array[$i])
           $max = $array[$i];
    return $max;      
}

// Returns maximum in array
function getMin($array)
{
   $n = count($array);
   $min = $array[0];
   for ($i = 1; $i < $n; $i++)
       if ($min > $array[$i])
           $min = $array[$i];
    return $min;      
}

// Driver code
$array = array(1, 2, 3, 4, 5);
echo(getMax($array));
echo("\n");
echo(getMin($array));
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
5
1
```

**方法 2(使用库函数)：**我们使用库函数来查找最小值和最大值。

1.  **max()：**max()根据标准比较返回被认为是“最高”的参数值。 如果多个不同类型的值求值相等(例如，0 和‘abc’)，则将返回第一个提供给函数的值。

2.  **min()：**min()返回根据标准比较被认为是“最低”的参数值。 如果多个不同类型的值求值相等(例如，0 和‘abc’)，将返回第一个提供给函数的值。

## PHP

```php
<?php
$array = array(1, 2, 3, 4, 5);
echo(max($array));
echo("\n");
echo(min($array));
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
5
1
```