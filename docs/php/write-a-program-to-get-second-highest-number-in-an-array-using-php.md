# 用 PHP 编写程序获取数组中第二高的数字？

> 原文:[https://www . geesforgeks . org/write-a-program-to-get-第二高数组中的数字-使用-php/](https://www.geeksforgeeks.org/write-a-program-to-get-second-highest-number-in-an-array-using-php/)

给定一个整数数组，任务是编写一个程序，高效地找到数组中的第二大元素。

**示例:**

```
Input: arr[] = {13, 14, 15, 16, 17, 18}
Output: The second largest element is 17.
Explanation: The largest element of the array
is 35 and the second largest element is 17

Input: arr[] = {10, 5, 10}
Output: The second largest element is 5.
Explanation: The largest element of the array
is 10 and the second largest element is 5

Input: arr[] = {10, 10, 10}
Output: The second largest does not exist.
Explanation: Largest element of the array  
is 10 there is no second largest element
```

**简单解决方案:**

**方法:**思路是先对数组进行降序排序，然后从排序后的数组中返回不等于最大元素的第二个元素。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
function bubbleSort(&$arr) {
    $n = sizeof($arr);

    // Traverse through all array elements
    for($i = 0; $i < $n; $i++) {
        $swapped = False;

        // Last i elements are already
        // in place
        for ($j = 0; $j < $n - $i - 1; $j++) {

            // traverse the array from 0 to
            // n-i-1\. Swap if the element
            // found is greater than the
            // next element
            if ($arr[$j] <$arr[$j+1]) {
                $t = $arr[$j];
                $arr[$j] = $arr[$j+1];
                $arr[$j+1] = $t;
                $swapped = True;
            }
        }

        // IF no two elements were swapped
        // by inner loop, then break
        if ($swapped == False)
            break;
    }
}

// Driver code to test above
$arr = array(64, 34, 25, 12, 22, 11, 90);
$len = sizeof($arr);
bubbleSort($arr);

if($arr[0] == $arr[1]) {
  echo "No element";
}
else {
  echo "Second Largest element is ".$arr[1];
}

?>
```

 **Output**

```
Second Largest element is 64
```

**复杂度分析:**

> **最坏和平均情况时间复杂度:** O(n*n)。当数组被反向排序时会出现最坏的情况。
> **最佳案例时间复杂度:** O(n)。最佳情况发生在数组已经排序的时候。
> **辅助空间:** O(1)
> 
> **边界情况:**当元素已经排序时，冒泡排序花费的时间最少(n 阶)。
> T3】排序到位:是
> T6】稳定:是

**另一种方法:**在单次遍历中找到第二大元素。

下面是完成此操作的完整算法:

```
1) Initialize the first as 0 (i.e, index of arr[0] element)
2) Start traversing the array from array[1],
  a) If the current element in array say arr[i] is greater
     than first. Then update first and second as,
     second = first
     first = arr[i]
  b) If the current element is in between first and second,
     then update second to store the value of current variable as
     second = arr[i]
3) Return the value stored in second.
```

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to find second largest
// element in an array

// Function to print the
// second largest elements
function print2largest($arr, $arr_size) {

    // There should be atleast
    // two elements
    if ($arr_size < 2) {
        echo(" Invalid Input ");
        return;
    }

    $first = $second = PHP_INT_MIN;

    for ($i = 0; $i < $arr_size ; $i++) {

        // If current element is
        // smaller than first
        // then update both
        // first and second
        if ($arr[$i] > $first) {
            $second = $first;
            $first = $arr[$i];
        }

        // If arr[i] is in
        // between first and
        // second then update
        // second
        else if ($arr[$i] > $second &&
                $arr[$i] != $first)
            $second = $arr[$i];
    }
    if ($second == PHP_INT_MIN)
        echo("There is no second largest element\n");
    else
        echo("The second largest element is "
                 . $second . "\n");
}

// Driver Code
$arr = array(12, 35, 1, 10, 34, 1);
$n = sizeof($arr);
print2largest($arr, $n);

?>
```

**Output**

```
The second largest element is 34
```