# 用 PHP 写程序显示任意数字的反转？

> 原文:[https://www . geesforgeks . org/write-a-program-to-display-reverse-of-any-number-in-PHP/](https://www.geeksforgeeks.org/write-a-program-to-display-reverse-of-any-number-in-php/)

写一个程序来反转整数的数字。

**示例:**

```php
Input : num = 12345
Output: 54321

Input : num = 876
Output: 678
```

可以使用*迭代方式*或*递归方式*来实现

**迭代方法:**

**算法:**

```php
Input:  num
(1) Initialize rev_num = 0
(2) Loop while num > 0
    (a) Multiply rev_num by 10 and add remainder
        of num divide by 10 to rev_num
        rev_num = rev_num*10 + num%10;
    (b) Divide num by 10
(3) Return rev_num
```

**示例:**

> num = 456213
> rev _ num = 0
> rev _ num = rev _ num * 10+num % 10 = 3
> num = num/10 = 45621
> rev _ num = rev _ num * 10+num % 10 = 20+6 = 31
> num = num/10 = 4562
> rev _ num = rev _ num * 10+num % 10 rev _ num = rev _ num * 10+num % 10 = 2650+4 = 31265
> num = num/10 = 4
> rev _ num = rev _ num * 10+num % 10 = 2650+4 = 312654
> num = num/10 = 0

**程序:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Iterative function to
// reverse digits of num
function reversDigits($num) {
    $rev_num = 0;
    while($num > 1) {
        $rev_num = $rev_num * 10 + $num % 10;
        $num = (int)$num / 10;
    }
    return $rev_num;
}

// Driver Code
$num = 456213;
echo "Original number is :".$num;
echo "\r\n";
echo "Reverse of no. is ", reversDigits($num);
?>
```

**Output**

```php
Original number is :456213
Reverse of no. is 312654
```

**时间复杂度:** O(log(n))，其中 n 为输入数。

**辅助空间:** O(1)

**递归方法:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program to reverse
// digits of a number
$rev_num = 0;
$base_pos = 1;

/* Recursive function to
reverse digits of num*/
function reversDigits($num) {
    global $rev_num;
    global $base_pos;
    if($num > 0) {
        reversDigits((int)($num / 10));
        $rev_num += ($num % 10) *
                    $base_pos;
        $base_pos *= 10;
    }
    return $rev_num;
}

// Driver Code
$num = 456213;
echo "Original number is :".$num;
echo "\r\n";
echo "Reverse of no. is ",
    reversDigits($num);

?>
```

**Output**

```php
Original number is :456213
Reverse of no. is 312654
```

**时间复杂度:** O(log(n))，其中 n 为输入数。