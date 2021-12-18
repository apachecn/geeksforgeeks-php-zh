# PHP|ds\Set Reduce()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-reduce-function/](https://www.geeksforgeeks.org/php-dsset-reduce-function/)

**ds\set：：Reduce()**函数是 PHP 中的一个内置函数，用于通过使用回调函数应用操作将集合缩减为单个值。

**语法：**

```
*mixed* public Ds\Set::reduce ( callable $callback 
[, mixed $initial ] )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$callback:** this parameter holds functions that contain operations on elements and store carry. The callback function takes two parameters: Carry and Value, where Carry is the value returned by the function and value is the value of the element in the current iteration.
*   **$Initial:** this parameter holds the initial value of carry and can be empty.

**返回值：**此函数返回回调函数返回的最终值。

以下程序说明了 PHP 中的**ds\set：：Reduce()**函数：

**程序 1：**

```
<?php 

// Declare new Set 
$set = new \Ds\Set([1, 2, 3, 4, 5]); 

echo("Set Elements\n"); 

print_r($set); 

// Callback function with reduce function 
echo("\nElement after performing operation\n"); 

var_dump($set->reduce(function($carry, $element) { 
    return $carry + $element + 2; 
})); 

?> 
```

**输出：**

```
Set Elements
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)

Element after performing operation
int(25)

```

**程序 2：**

```
<?php 

// Declare new Set
$set = new \Ds\Set([10, 20, 30, 40, 50]); 

echo("Original set elements\n"); 

print_r($set); 

$func_gfg = function($carry, $element) { 
    return $carry * $element; 
}; 

echo("\nSet after reducing to single element\n"); 

// Use reduce() function 
var_dump($set->reduce($func_gfg, 10)); 

?> 
```

**输出：**

```
Original set elements
Ds\Set Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
)

Set after reducing to single element
int(120000000)

```

**引用：**[https://www.php.net/manual/en/ds-set.reduce.php](https://www.php.net/manual/en/ds-set.reduce.php)