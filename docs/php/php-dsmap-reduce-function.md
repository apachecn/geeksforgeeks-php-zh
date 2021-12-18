# PHP|ds\Map Reduce()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-reduce-function/](https://www.geeksforgeeks.org/php-dsmap-reduce-function/)

**ds\Map：：Reduce()**函数是 PHP 中的一个内置函数，用于通过使用回调函数应用操作将映射减少到单个值。

**语法：**

```
*mixed* public Ds\Map::reduce( $callback, $initial )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$callback:** this parameter holds functions that contain operations on elements and store carry. This callback function contains three parameters listed below:
    *   **Carry:** it holds the return value of the previous callback, or Initial if it is the first iteration.
    *   **key:** saves the key for the current iteration.
    *   **value:** it holds the value of the current iteration.
*   **$Initial:** this parameter holds the initial value of carry and can be empty.

**返回值：**此函数返回回调函数返回的最终值。

以下程序说明了 PHP 中的**ds\Map：：Reduce()**函数：

**程序 1：**

```
<?php 

// Declare a new map
$map = new \Ds\Map(["a" => 1, "b" => 3, "c" => 5]); 

echo("Map Elements\n"); 

print_r($map); 

// Callback function with reduce function 
echo("\nElement after performing operation\n"); 

var_dump($map->reduce(function($carry, $key, $element) { 
    return $carry + $element + 2; 
})); 

?> 
```

**输出：**

```
Map Elements
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 5
        )

)

Element after performing operation
int(15)

```

**程序 2：**

```
<?php 

// Declare new Map elements
$map = new \Ds\Map(["a" => 10, "b" => 20,
            "c" => 30, "d" => 40, "e" => 50]); 

echo("Original map elements\n"); 

print_r($map); 

$func_gfg = function($carry, $key, $element) { 
    return $carry * $element; 
}; 

echo("\nMap after reducing to single element\n"); 

// Use reduce() function 
var_dump($map->reduce($func_gfg, 10)); 

?> 
```

**输出：**

```
Original map elements
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 10
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 20
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 30
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 40
        )

    [4] => Ds\Pair Object
        (
            [key] => e
            [value] => 50
        )

)

Map after reducing to single element
int(120000000)

```

**引用：**[https://www.php.net/manual/en/ds-map.reduce.php](https://www.php.net/manual/en/ds-map.reduce.php)