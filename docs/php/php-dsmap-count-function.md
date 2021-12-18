# PHP|ds\Map count()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-count-function/](https://www.geeksforgeeks.org/php-dsmap-count-function/)

**ds\Map：：Count()**函数是 PHP 中的一个内置函数，用于计算 Map 中存在的元素数量。 它还提到了地图的大小。

**语法：**

```
*int* public Ds\Map::count()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Map 中存在的元素数量。

以下程序说明了 PHP 中的**ds\Map：：Count()**函数：

**程序 1：**

```
<?php 
// PHP program to illustrate the count() 
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map([
    "1" => "Geeks",  
    "2" => "for",
    "3" => "Geeks"
]); 

// Display the map elements
print_r($map); 

echo "Number of elements present in map: ";
print_r($map->count());

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

)
Number of elements present in map: 3

```

**程序 2：**

```
<?php 
// PHP program to illustrate the count() 
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map(["1" => "10", 
            "2" => "20", "3" => 30, "4" => 40]); 

// Print map elements
print_r($map); 

echo "Number of elements present in map: ";
print_r($map->count());

echo "\n";

// Creating another Map 
$map = new \Ds\Map([1 => "Welcome", 
            2 => "to", 3 => "GeeksforGeeks"]); 

// Print map elements
print_r($map); 

echo "Number of elements present in map: ";
print_r($map->count());

?> 
```

**输出：**

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => 10
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => 20
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => 30
        )

    [3] => Ds\Pair Object
        (
            [key] => 4
            [value] => 40
        )

)
Number of elements present in map: 4
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => Welcome
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => to
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => GeeksforGeeks
        )

)
Number of elements present in map: 3

```

**引用：**[https://www.php.net/manual/en/ds-map.count.php](https://www.php.net/manual/en/ds-map.count.php)