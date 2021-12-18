# PHP|ds\Map Remove()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-remove-function/](https://www.geeksforgeeks.org/php-dsmap-remove-function/)

**ds\Map：：Remove()函数**是 PHP 中的一个内置函数，用于通过键删除和返回值。

**语法：**

```
*mixed* Ds\Map::remove( $key, $default )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$key:** it holds the key values that need to be deleted.
*   **$DEFAULT:** optional parameter, returned if KEY is not found.

**返回值：**此函数返回删除的值。

**异常：**如果键不存在且未提供$default 的值，则此函数引发 OutOfRangeException。

下面的程序说明了 PHP 中的 Ds\Map：：Remove()函数：

**示例 1：**

```
<?php 

// Declare new Map 
$map = new \Ds\Map([
    1 => "geeks",
    2 => "for", 
    3 => "geeks",
    4 => "DataStructures"
]); 

echo("Map Elements\n"); 

// Display the map elements 
print_r($map); 

echo("\nRemoved element of the map: \n"); 

// Use remove() function to remove 
// value at index 3 and return it 
var_dump($map->remove(3)); 

?>
```

**输出：**

```
Map Elements
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => for
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => geeks
        )

    [3] => Ds\Pair Object
        (
            [key] => 4
            [value] => DataStructures
        )

)

Removed element of the map: 
string(5) "geeks"

```

**示例：**

```
<?php 

// Declare new Map 
$map = new \Ds\Map([
    "a" => "geeks",
    "b" => "for", 
    "c" => "geeks",
    "d" => "DataStructures"
]); 

echo("Map Elements\n"); 

// Display the map elements 
print_r($map); 

echo("\nRemoved element of the map: \n"); 

// Use remove() function to remove 
// value at index 3 and return it 
var_dump($map->remove("c")); 

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
            [value] => geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => for
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => geeks
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => DataStructures
        )

)

Removed element of the map: 
string(5) "geeks"

```

**引用：**[https://www.php.net/manual/en/ds-map.remove.php](https://www.php.net/manual/en/ds-map.remove.php)