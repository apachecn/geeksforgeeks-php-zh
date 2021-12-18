# PHP|ds\Map Skip()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-skip-function/](https://www.geeksforgeeks.org/php-dsmap-skip-function/)

**ds\Map：：Skip()**函数是 PHP 中的一个内置函数，用于返回给定位置索引处的对。

**语法：**

```
*Ds\Pair* public Ds\Map::skip ( int $position )

```

**参数：**此函数接受单个参数**$position**，该参数用于返回从零开始的位置索引。

**返回值：**它返回给定位置的 Ds\对。

以下程序说明了 PHP 中的**ds\Map：：Skip()**函数：

**程序 1：**

```
<?php 

// Declare a new map
$map = new \Ds\Map(["a" => 1, "b" => 3, "c" => 5]); 

print_r($map->skip(1));

// Declare another new map
$map = new \Ds\Map(["1" => "Geeks", "2" => "for", 
                                  "3" => "Geeks"]); 

print_r($map->skip(2));

?>
```

**输出：**

```
Ds\Pair Object
(
    [key] => b
    [value] => 3
)
Ds\Pair Object
(
    [key] => 3
    [value] => Geeks
)

```

**程序 2：**

```
<?php 

// Declare a new map
$map = new \Ds\Map(["Geeks1" => "computer", 
 "Geeks2" => "science", "Geeks3" => 5, "Geeks4" => 20]); 

print_r($map->skip(0));

// Declare another new map
$map = new \Ds\Map(["x" => "A", "y" => "B", "z" => "C"]); 

print_r($map->skip(1));

?>
```

**输出：**

```
Ds\Pair Object
(
    [key] => Geeks1
    [value] => computer
)
Ds\Pair Object
(
    [key] => y
    [value] => B
)

```

**引用：**[https://www.php.net/manual/en/ds-map.skip.php](https://www.php.net/manual/en/ds-map.skip.php)