# PHP 中的匿名递归函数

> 原文:[https://www . geesforgeks . org/anonymous-recursive-function-in-PHP/](https://www.geeksforgeeks.org/anonymous-recursive-function-in-php/)

匿名递归函数是一种递归类型，在这种递归中，函数不通过名称显式调用另一个函数。这可以通过使用更高阶的函数作为参数传入一个函数并调用该函数来全面完成。它可以通过反射特性隐式地完成，反射特性允许用户根据当前上下文，尤其是当前函数来访问某些函数。
在计算机科学的理论中，匿名递归是有意义的，因为匿名递归是一种无需命名函数就可以实现递归的递归类型。

**匿名递归的使用:**

*   匿名递归主要用于允许匿名函数的递归。
*   特别是当它们形成闭包或用作回调时，以避免必须绑定函数的名称。

**替代品:**

*   命名递归和命名函数的使用。
*   如果给定了匿名函数，匿名递归可以通过将名称绑定到函数来完成，就像在命名函数中一样。

**程序 1:**

```php
<?php 
// PHP program to illustrate the 
// Anonymous recursive function 

$func = function ($limit = NULL) use (&$func) { 
    static $current = 10; 

    // if condition to check value of $current.
    if ($current <= 0) { 
        //break the recursion 
        return FALSE;
    } 

    // Print value of $current.
    echo "$current\n"; 

    $current--; 

    $func(); 
}; 

//  Function call
$func();
?>
```

**Output:**

```php
10
9
8
7
6
5
4
3
2
1

```

**程序 2:**

```php
<?php
// PHP program to illustrate the 
// Anonymous recursive function 

$factorial = function( $num ) use ( &$factorial ) {

    // Base condition of recursion
    if( $num == 1 ) 
        return 1;

    // return statement when $m is not equals to 1.
    return $factorial( $num - 1 ) * $num;
};

// Function call
print $factorial( 6 );
?>
```

**Output:**

```php
720

```