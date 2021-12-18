# PHP|ds\Sequence Reduce()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-reduce-function/](https://www.geeksforgeeks.org/php-dssequence-reduce-function/)

**Ds\Sequence：：Reduce()**函数是 PHP 中的一个内置函数，用于使用回调函数将序列缩减为单个值。

**语法：**

```
*mixed* abstract public Ds\Sequence::reduce ( callable $callback 
[, mixed $initial ] )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$callback:** this parameter holds functions that contain operations on elements and store carry. The callback function contains two parameters, Carry and Value, where Carry is the value returned by the function and value is the value of the element in the current iteration.
*   **$Initial:** this parameter holds the initial value of carry and can be empty.

**返回值：**此函数返回回调函数的最终值。

以下程序说明了 PHP 中的**ds\Sequence：：Reduce()**函数：

**程序 1：**

```
<?php 

// Declare new sequence
$seq = new \Ds\Vector([1, 2, 3, 4, 5]); 

echo("Sequence Elements\n"); 

print_r($seq); 

// Callback function with reduce function 
echo("\nElement after performing operation\n"); 

var_dump($seq->reduce(function($carry, $element) { 
    return $carry + $element + 2; 
})); 

?> 
```

**输出：**

```
Sequence Elements
Ds\Vector Object
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

// Declare new sequence
$seq = new \Ds\Vector([10, 20, 30, 40, 50]); 

echo("Original sequence elements\n"); 

print_r($seq); 

$func_gfg = function($carry, $element) { 
    return $carry * $element; 
}; 

echo("\nSequence after reducing to single element\n"); 

// Use reduce() function 
var_dump($seq->reduce($func_gfg, 10)); 

?> 
```

**输出：**

```
Original sequence elements
Ds\Vector Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
)

Sequence after reducing to single element
int(120000000)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.reduce.php](https://www.php.net/manual/en/ds-sequence.reduce.php)