# PHP 中如何从函数返回多个值？

> 原文:[https://www . geesforgeks . org/如何从 php 中的函数返回多个值/](https://www.geeksforgeeks.org/how-to-return-multiple-values-from-function-in-php/)

PHP 不支持在一个函数中返回多个值。在函数内部，当执行第一个 return 语句时，它会将控制权交还给调用函数，而第二个 return 语句将永远不会被执行。但是，有一些方法可以解决这个限制。
可以使用数组从函数中返回多个值。

**示例 1:** 这个示例展示了如何在 PHP 中从一个函数返回多个值。首先，创建一个空数组，将元素推入数组，然后返回数组。

```php
<?php

// Function to return the array
// of factors of n
function factors( $n ) { 

    // Declare an empty array
    $fact = array();

    // Loop to find the 
    for ( $i = 1; $i < $n; $i++) { 

        // Check if i is the factor of
        // n then pusj it into array
        if( $n % $i == 0 )
            array_push( $fact, $i );
    }

    // Return the array
    return $fact;
} 

// Declare a variable and initialize it
$num = 24;

// Function call
$nFactors = factors($num);

// Display the result
echo 'Factors of ' . $num . ' are: <br>';

foreach( $nFactors as $x ) {
    echo $x . "<br>";
}

?>
```

**Output:**

```php
Factors of 24 are: 
1
2
3
4
6
8
12

```

**示例 2:** 本示例使用[列表](https://www.geeksforgeeks.org/php-list-function/)功能存储变量的交换值。它用于同时向多个变量分配数组值。可以使用 list()将函数在数组中返回的多个值分配给相应的变量。

```php
<?php

// Function to swap two numbers
function swap( $x, $y ) { 
    return array( $y, $x );
} 

// Declare variable and initialize it
$a = 10;
$b = 20;

echo 'Before swapping the elements <br>';

// Display the value of a and b
echo 'a = ' . $a . '<br>' . 'b = ' . $b . '<br>';

// Function call to swap the value of a and b
list($a, $b) = swap($a, $b);

echo 'After swapping the elements <br>';

// Display the value of a and b
echo 'a = ' . $a . '<br>' . 'b = ' . $b . '<br>';

?>
```

**Output:**

```php
Before swapping the elements 
a = 10
b = 20
After swapping the elements 
a = 20
b = 10

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。