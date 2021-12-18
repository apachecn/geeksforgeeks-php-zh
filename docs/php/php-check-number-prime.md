# PHP |检查一个数字是否是质数

> 原文:[https://www.geeksforgeeks.org/php-check-number-prime/](https://www.geeksforgeeks.org/php-check-number-prime/)

给定一个数字，我们需要在 PHP 中检查它是否是质数。主要检查的一般方法在这里讨论。在本文中，我们将学习如何在 PHP 中检查一个数字是否是质数。

示例:

```php
Input : 21
Output : Not Prime

Input : 31
Output : Prime

```

**简单方法:**
一个简单的解决方法是迭代从 2 到 n/2 的所有数字，对于每个数字检查它是否除 n，如果我们找到任何除的数字，我们返回 0(假)，否则我们将返回 1(真)。

下面是这个方法在 PHP 中的实现:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP code to check whether a number is prime or Not
// function to check the number is Prime or Not
function primeCheck($number){
    if ($number == 1)
    return 0;
    for ($i = 2; $i <= $number/2; $i++){
        if ($number % $i == 0)
            return 0;
    }
    return 1;
}

// Driver Code
$number = 31;
$flag = primeCheck($number);
if ($flag == 1)
    echo "Prime";
else
    echo "Not Prime"
?>
```

输出:

```php
Prime
```

时间复杂度:0(n)

**高效方法:**
我们可以通过观察来优化上述方法，我们可以检查直到 n，而不是检查直到 sqrt(n)，因为 n 的较大因子必须是已经检查过的较小因子的倍数。
所以，我们将在[2，sqrt(number)]范围内遍历，检查该数是否能被任意数整除。如果它能被整除，它就不是质数。

下面是这个方法在 PHP 中的实现:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP code to check whether a number is prime or Not
// function to check the number is Prime or Not
function primeCheck($number){
    if ($number == 1)
    return 0;

    for ($i = 2; $i <= sqrt($number); $i++){
        if ($number % $i == 0)
            return 0;
    }
    return 1;
}

// Driver Code
$number = 31;
$flag = primeCheck($number);
if ($flag == 1)
    echo "Prime";
else
    echo "Not Prime"
?>
```

输出:

```php
Prime
```

时间复杂度:O(sqrt(n))