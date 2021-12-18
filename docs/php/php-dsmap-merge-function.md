# PHP|ds\Map Merge()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-merge-function/](https://www.geeksforgeeks.org/php-dsmap-merge-function/)

**ds\Map：：Merge()**函数是 PHP 中的一个内置函数，用于返回添加所有给定关联的结果。

**语法：**

```
*Ds\Map* public Ds\Map::merge( $values )
```

**参数：**此函数接受保存可遍历对象或数组的单个参数**$values**。

**返回值：**此函数返回将给定的可遍历对象或数组的所有键与其相应值相关联，并结合当前实例。

以下程序说明了 PHP 中的**ds\Map：：Merge()**函数：

**程序 1：**

```
<?php 

// Create new map
$map = new \Ds\Map(["a" => 12,
    "b" => 15, "c" => 18, "d" => 20]); 

// Merge the map element and display it 
print_r($map->merge(["a" => 1, "c" => 2, "f" => 3])); 

// Display the set element 
print_r($map) 

?> 
```

**输出：**

```
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
            [value] => 15
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 2
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 20
        )

    [4] => Ds\Pair Object
        (
            [key] => f
            [value] => 3
        )

)
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 12
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 15
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 18
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 20
        )

)

```

**程序 2：**

```
<?php 

// Create new map
$map = new \Ds\Map(["1" => "Geeks",
        "2" => "for", "3" => "Geeks"]); 

// Merge the map element and display it 
print_r($map->merge(["a" => "Computer",
        "b" => "Science", "c" => "Portal"])); 

?> 
```

**输出：**

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => Geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => for
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => Geeks
        )

    [3] => Ds\Pair Object
        (
            [key] => a
            [value] => Computer
        )

    [4] => Ds\Pair Object
        (
            [key] => b
            [value] => Science
        )

    [5] => Ds\Pair Object
        (
            [key] => c
            [value] => Portal
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.merge.php](https://www.php.net/manual/en/ds-map.merge.php)