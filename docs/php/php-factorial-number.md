# PHP|数的阶乘

> Original: [https://www.geeksforgeeks.org/php-factorial-number/](https://www.geeksforgeeks.org/php-factorial-number/)

我们已经知道如何在其他语言中得到一个数的阶乘。 让我们看看如何在 PHP 中使用递归和非递归方式实现这一点。

例如：

```php
Input : 5
Output : 120

Input : 10
Output : 3628800

```

**方法 1：迭代方式**
在此方法中，我们简单地使用 for 循环迭代数字序列以获得阶乘。

```php
<?php
// PHP code to get the factorial of a number
// function to get factorial in iterative way
function Factorial($number){
    $factorial = 1;
    for ($i = 1; $i <= $number; $i++){
      $factorial = $factorial * $i;
    }
    return $factorial;
}

// Driver Code
$number = 10;
$fact = Factorial($number);
echo "Factorial = $fact";
?>
```

产出：

```php
3628800

```

**方法 2：使用递归**
在此方法中，我们调用相同的方法来获得阶乘的序列。

```php
<?php
// PHP code to get the factorial of a number
// function to get factorial in iterative way
function Factorial($number){
    if($number <= 1){  
        return 1;  
    }  
    else{  
        return $number * Factorial($number - 1);  
    }  
}

// Driver Code
$number = 10;
$fact = Factorial($number);
echo "Factorial = $fact";
?>
```

产出：

```php
3628800

```