# PHP|Ds\Vector Reduce()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-reduce-function/](https://www.geeksforgeeks.org/php-dsvector-reduce-function/)

**Ds\Vector：：Reduce()**函数是 PHP 中的一个内置函数，它通过在回调函数中应用操作将向量减少到单个值。

**语法：**

```
*mixed * public Ds\Vector::reduce( $callback, $initial )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$callback:** this parameter holds functions that contain operations on elements and store carry. The callback function takes two parameters: Carry and Value, where Carry is the value returned by the function and value is the value of the element in the current iteration.
*   **$Initial:** this parameter holds the initial value of carry and can be empty.

**返回值：**此函数返回回调函数返回的最终值。

以下程序说明了 PHP 中的**ds\Vector：：Reduce()**函数：

**程序 1：**

```
<?php

// Declare new Vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5]);

echo("Vector Elements\n");

print_r($vect);

// callback function with reduce function
echo("\nElement after performing operation\n");
var_dump($vect->reduce(function($carry, $element) {
    return $carry + $element + 2;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Declare new Vector
$vect = new \Ds\Vector([10, 20, 30, 40, 50]);

echo("Original vector elements\n");

print_r($vect);

$func_gfg = function($carry, $element) {
    return $carry * $element;
};

echo("\nVector after reducing to single element\n");

// Use reduce() function
var_dump($vect->reduce($func_gfg, 10));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.reduce.php](http://php.net/manual/en/ds-vector.reduce.php)