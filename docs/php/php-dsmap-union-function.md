# PHP|ds\Map Union()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-union-function/](https://www.geeksforgeeks.org/php-dsmap-union-function/)

Ds\Map：：Union()函数是 PHP 中的一个内置函数，用于创建包含两个映射并集的新映射。

**语法：**

```php
Ds\Map Ds\Map::union( $map )
```

**参数：**此函数接受单个参数**$map**，该参数用于保存要与当前实例组合的实例的另一个映射。

**返回值：**它返回一个包含两个映射的并集的映射。

下面的程序说明了 PHP 中的 Ds\Map：：Union()函数：

**程序 1：**

```php
<?php 

// Declare a new map
$a = new \Ds\Map(["a" => 1, "b" => 3, "c" => 5]); 

// Declare another new map
$b = new \Ds\Map(["a" => 2, "c" => 3, "d" => 6]); 

// Print the Union of two map
echo("Union of both map is: \n"); 

print_r($a->union($b));

?>
```

**输出：**

```php
Union of both map is: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 6
        )

)

```

**程序 2：**

```php
<?php 

// Declare a new map
$a = new \Ds\Map(["a" => "Geeks", "b" => "for", "c" => "Geeks"]); 

// Declare another new map
$b = new \Ds\Map(["b" => "Computer", "e" => "Science", "f" => "Portal"]); 

// Print the union of two map
echo("Union of both map is: \n"); 

print_r($a->union($b));

?>
```

**输出：**

```php
Union of both map is: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => Geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => Computer
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => Geeks
        )

    [3] => Ds\Pair Object
        (
            [key] => e
            [value] => Science
        )

    [4] => Ds\Pair Object
        (
            [key] => f
            [value] => Portal
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.union.php](https://www.php.net/manual/en/ds-map.union.php)