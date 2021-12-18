# PHP|ds\Map ksorted()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-ksorted-function/](https://www.geeksforgeeks.org/php-dsmap-ksorted-function/)

**ds\Map：：ksorted()**函数是 PHP 中的内置函数，用于返回按键排序的副本。

**语法：**

```php
*Ds\Map* public Ds\Map::ksorted ([ callable $comparator ] )

```

**参数：**此函数接受单个参数**$compator**，该参数包含对映射副本进行排序时将根据其比较值的函数。 比较器应该根据作为参数传递给它的两个值的比较返回下列值：

*   1, if the first element is expected to be smaller than the second element.
*   -1, if the first element is expected to be larger than the second element.
*   0, if the first element is expected to be equal to the second element.

**返回值：**此函数返回按键排序的 map 副本。

以下程序说明了 PHP 中的**ds\Map：：ksorted()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate ksorted() function 

// Declare a Map 
$map = new \Ds\Map([1 => 20, 3 => 10, 2 => 30]); 

// Print the sorted copy of Map by key
print_r($map->ksorted()); 

?>
```

**输出：**

```php
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

```php
<?php 
// PHP program to illustrate ksorted() function 

// Declare a Map 
$map = new \Ds\Map(["x" => "Geeks",
        "a" => "for", "z" => "Geeks"]); 

// Print the sorted copy Map 
print_r($map->ksorted()); 

?> 
```

**输出：**

```php
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

**引用：**[https://www.php.net/manual/en/ds-map.ksorted.php](https://www.php.net/manual/en/ds-map.ksorted.php)