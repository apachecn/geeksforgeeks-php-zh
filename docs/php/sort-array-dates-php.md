# 在 PHP 中对日期数组进行排序

> 原文:[https://www.geeksforgeeks.org/sort-array-dates-php/](https://www.geeksforgeeks.org/sort-array-dates-php/)

我们得到了一个由(Y-m-d)格式的多个日期组成的数组。我们必须用 PHP 编写一个程序，按照降序对数组中的所有日期进行排序。

示例:

```
Input : array("2018-06-04", "2014-06-08", "2018-06-05")
Output : 2018-06-05  2018-06-04  2014-06-08

Input : array("2016-09-12", "2009-09-08", "2009-09-09")
Output : 2016-09-12  2009-09-09  2009-09-08

```

为了在 C/C++/Java 或任何其他通用编程语言中解决这个问题，我们必须要么基于年、月来比较日期，要么通过将它们存储在任何结构或任何其他期望的数据结构中来最终根据天来比较日期。但是在 PHP 中，如果我们应用 strtotime()函数，这个问题似乎非常容易。strtotime()函数是一个 PHP 函数，它将任意格式的给定日期更改为时间戳，时间戳本质上是一个大整数，然后在对数组进行排序时，我们可以通过定义一个比较器函数来轻松使用 [PHP | usort()函数](https://www.geeksforgeeks.org/php-usort-function/)。比较器函数将接受两个日期参数，这两个参数将使用 strtotime()函数转换为整数时间戳，然后与基于整数时间戳值的排序日期进行比较。

**使用的内置函数:**

*   *strtotime ():* This function changes the given date string to a timestamp (large int value).
*   *[usort ()](https://www.geeksforgeeks.org/php-usort-function/) :* This function sorts the given array according to the comparison function defined by the user.

下面是上面思路的 PHP 实现:

```
<?php
// PHP program to sort array of dates 

// user-defined comparison function 
// based on timestamp
function compareByTimeStamp($time1, $time2)
{
    if (strtotime($time1) < strtotime($time2))
        return 1;
    else if (strtotime($time1) > strtotime($time2)) 
        return -1;
    else
        return 0;
}

// Input Array
$arr = array("2016-09-12", "2009-09-06", "2009-09-09");

// sort array with given user-defined function
usort($arr, "compareByTimeStamp");

print_r($arr);

?>
```

输出:

```
Array
(
    [0] => 2016-09-12
    [1] => 2009-09-09
    [2] => 2009-09-06
)

```