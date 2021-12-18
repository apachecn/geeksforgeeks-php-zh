# PHP|ds\Map xor()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-xor-function/](https://www.geeksforgeeks.org/php-dsmap-xor-function/)

**ds\Map：：XOR()**函数是 PHP 中的一个内置函数，用于创建一个新映射，该映射包含第一个映射或第二个映射中的值，但不能同时包含这两个映射中的值。

**语法：**

```php
*Ds\Map* public Ds\Map::xor ( Ds\Map $map )

```

**参数：**此参数保存另一个值映射。

**返回值：**返回一个包含当前地图与另一个地图的异或的地图。

下面的程序说明了 PHP 中的**ds\Map：：XOR()**函数：

**程序 1：**

```php
<?php 

// Declare a new map
$a = new \Ds\Map(["a" => 1, "b" => 3, "c" => 5]); 

// Declare another new map
$b = new \Ds\Map(["a" => 2, "c" => 3, "d" => 6]); 

// Print the xor of two map
echo("xor of both map is: \n"); 

print_r($a->xor($b));

?>
```

**输出：**

```php
xor of both map is: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [1] => Ds\Pair Object
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
$a = new \Ds\Map(["a" => "Geeks", "b" => "for", 
                                          "c" => "Geeks"]); 

// Declare another new map
$b = new \Ds\Map(["b" => "Computer", "e" => "Science",
                                         "f" => "Portal"]); 

// Print the xor of two map
echo("xor of both map is: \n"); 

print_r($a->xor($b));

?>
```

**输出：**

```php
xor of both map is: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => Geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => c
            [value] => Geeks
        )

    [2] => Ds\Pair Object
        (
            [key] => e
            [value] => Science
        )

    [3] => Ds\Pair Object
        (
            [key] => f
            [value] => Portal
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.xor.php](https://www.php.net/manual/en/ds-map.xor.php)