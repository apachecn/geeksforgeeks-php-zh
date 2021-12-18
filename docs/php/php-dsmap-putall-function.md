# PHP|ds\Map putAll()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-putall-function/](https://www.geeksforgeeks.org/php-dsmap-putall-function/)

**ds\Map：：putAll()**函数是 PHP 中的内置函数，用于关联可遍历对象或数组的所有键-值对。

**语法：**

```php
*void* public Ds\Map::putAll( mixed $pairs )
```

**参数：**此函数接受作为遍历对象或数组的单个参数**$pains**。

**返回值：**不返回任何值。

以下程序说明了 PHP 中的**ds\Map：：putAll()**函数：

**程序 1：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map();

$map->putAll([
    "a" => "Geeks",
    "b" => "for",
    "c" => "Geeks"
]); 

print_r($map);

// Declare a new map
$map = new \Ds\Map();

$map->putAll([
    "b" => "Computer",
    "e" => "Science",
    "f" => "Portal"
]); 

print_r($map);

?>
```

**输出：**

```php
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
            [value] => for
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => Geeks
        )

)
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => b
            [value] => Computer
        )

    [1] => Ds\Pair Object
        (
            [key] => e
            [value] => Science
        )

    [2] => Ds\Pair Object
        (
            [key] => f
            [value] => Portal
        )

)

```

**程序 2：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map();

$map->putAll([
    "Geeks1" => "computer", 
    "Geeks2" => "science",
    "Geeks3" => 5,
    "Geeks4" => 20
]); 

var_dump($map);

// Declare a new map
$map = new \Ds\Map();

$map->putAll([
    "x" => "A", 
    "y" => "B",
    "z" => "C"
]); 

var_dump($map);

?>
```

**输出：**

```php
object(Ds\Map)#1 (4) {
  [0]=>
  object(Ds\Pair)#2 (2) {
    ["key"]=>
    string(6) "Geeks1"
    ["value"]=>
    string(8) "computer"
  }
  [1]=>
  object(Ds\Pair)#3 (2) {
    ["key"]=>
    string(6) "Geeks2"
    ["value"]=>
    string(7) "science"
  }
  [2]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    string(6) "Geeks3"
    ["value"]=>
    int(5)
  }
  [3]=>
  object(Ds\Pair)#5 (2) {
    ["key"]=>
    string(6) "Geeks4"
    ["value"]=>
    int(20)
  }
}
object(Ds\Map)#5 (3) {
  [0]=>
  object(Ds\Pair)#1 (2) {
    ["key"]=>
    string(1) "x"
    ["value"]=>
    string(1) "A"
  }
  [1]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    string(1) "y"
    ["value"]=>
    string(1) "B"
  }
  [2]=>
  object(Ds\Pair)#3 (2) {
    ["key"]=>
    string(1) "z"
    ["value"]=>
    string(1) "C"
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-map.putall.php](https://www.php.net/manual/en/ds-map.putall.php)