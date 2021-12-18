# PHP|ds\Map：：kort()函数

> Original: [https://www.geeksforgeeks.org/php-dsmapksort-function/](https://www.geeksforgeeks.org/php-dsmapksort-function/)

**ds\Map：：kort()**函数是 PHP 中的一个内置函数，用于按键对地图元素进行就地排序。

**语法：**

```
*void* public Ds\Map::ksort ([ callable $comparator ] )
```

**参数：**此函数接受单个参数**$compator**，该参数包含对映射副本进行排序时将根据其比较值的函数。 比较器应该根据作为参数传递给它的两个值的比较返回下列值：

*   1, if the first element is expected to be smaller than the second element.
*   -1, if the first element is expected to be larger than the second element.
*   0, if the first element is expected to be equal to the second element.

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**ds\Map：：kort()**函数：

**程序 1：**

```
<?php 
// PHP program to illustrate ksort() function 

// Declare a Map 
$map = new \Ds\Map([1 => 20, 3 => 10, 2 => 30]); 

// Sort the Map element by key
$map->ksort(); 

// Display the map element
print_r($map);

?>
```

**输出：**

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => 20
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => 30
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => 10
        )

)

```

**程序 2：**

```
<?php 
// PHP program to illustrate ksort() function 

// Declare a Map 
$map = new \Ds\Map(["x" => "Geeks",
        "a" => "for", "z" => "Geeks"]); 

// Sort the Map element by key
$map->ksort(); 

// Display sorted element
print_r($map);

?> 
```

**输出：**

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => for
        )

    [1] => Ds\Pair Object
        (
            [key] => x
            [value] => Geeks
        )

    [2] => Ds\Pair Object
        (
            [key] => z
            [value] => Geeks
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.ksort.php](https://www.php.net/manual/en/ds-map.ksort.php)