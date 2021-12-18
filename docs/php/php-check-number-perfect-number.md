# PHP |检查一个数字是否是完全数

> 原文:[https://www . geesforgeks . org/PHP-check-number-perfect-number/](https://www.geeksforgeeks.org/php-check-number-perfect-number/)

一个完全数如果等于它的因子之和，也就是原数等于它除了数本身以外的所有因子之和，就是一个数。在[这篇](https://www.geeksforgeeks.org/perfect-number/)文章中，我们已经讨论了如何检查一个数字是否完美。在本文中，我们将讨论如何在 PHP 中做到这一点。

示例:

```php
Input : 6
Output : Perfect Number
Explanation: factors of 6 are 1, 2, 3, 6
             sum of its factors (excluding the 
             number itself) = 1 + 2 + 3 = 6 

Input : 24
Output : Not Perfect Number
Explanation : factors of 24 are 1,2,3,4,6,8,12,24 
              sum of its factors(excluding the 
              number itself) = 1 + 2 + 3 + 4  
                                + 6 + 8 + 12 = 36

```

这个想法是，我们将遍历[1，N]范围内的每个数字，并检查它是否是给定数字 N 的因子。如果它是因子，我们将把这个数字添加到变量$sum 中。最后是变量$sum 等于原始数，那么给定的数就是一个完全数。

下面是上述思想在 PHP 中的实现:

```php
<?php
// Function to check if a number is perfect
function isPerfectNumber($N)
{
    // To store the sum
    $sum = 0;

    // Traversing through each number
    // In the range [1,N)
    for ($i = 1; $i < $N; $i++)
    {
        if ($N % $i == 0)
        {
            $sum = $sum + $i;
        }      
    }

    // returns True is sum is equal
    // to the original number.
    return $sum == $N;
}

// Driver's code
$N = 6;

if (isPerfectNumber($N))
    echo " Perfect Number";
else
    echo "Not  Perfect Number";
?>
```

输出:

```php
Perfect Number

```