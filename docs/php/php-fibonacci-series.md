# 加入时间：清华大学 2007 年 01 月 25 日下午 3：33

> Original: [https://www.geeksforgeeks.org/php-fibonacci-series/](https://www.geeksforgeeks.org/php-fibonacci-series/)

[斐波那契级数](https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/)是一系列元素，前两个元素相加得到下一个元素，从 0 和 1 开始。在本文中，我们将学习如何使用迭代和递归的方式在 PHP 中生成斐波纳契级数。 给定一个数字 n，我们需要找到直到第 n 项的斐波纳契级数。
示例：

```php
Input : 10
Output : 0 1  1 2 3 5 8 13 21 34

Input : 15
Output : 0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 

```

**方法 1：使用递归方式**
递归是一种重复调用同一函数直到基本条件匹配以结束递归的方式。

```php
<?php  
// PHP code to get the Fibonacci series
// Recursive function for fibonacci series.
function Fibonacci($number){

    // if and else if to generate first two numbers
    if ($number == 0)
        return 0;    
    else if ($number == 1)
        return 1;    

    // Recursive Call to get the upcoming numbers
    else
        return (Fibonacci($number-1) + 
                Fibonacci($number-2));
}

// Driver Code
$number = 10;
for ($counter = 0; $counter < $number; $counter++){  
    echo Fibonacci($counter),' ';
}
?>
```

产出：

```php
0 1  1 2 3 5 8 13 21 34

```

**方法 2：首先使用迭代方式**
将第一个和第二个数字初始化为 0 和 1，然后打印第一个和第二个数字。 然后，我们将流发送到迭代的 While 循环，在该循环中，我们通过将前两个数字相加得到下一个数字，同时我们将第一个数字与第二个数字交换，将第二个数字与第三个数字交换。

```php
<?php
// PHP code to get the Fibonacci series
function Fibonacci($n){

    $num1 = 0;
    $num2 = 1;

    $counter = 0;
    while ($counter < $n){
        echo ' '.$num1;
        $num3 = $num2 + $num1;
        $num1 = $num2;
        $num2 = $num3;
        $counter = $counter + 1;
    }
}

// Driver Code
$n = 10;
Fibonacci($n);
?>
```

产出：

```php
0 1  1 2 3 5 8 13 21 34

```