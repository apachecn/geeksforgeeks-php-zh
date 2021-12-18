# PHP|ds\Map put()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-put-function/](https://www.geeksforgeeks.org/php-dsmap-put-function/)

**ds\Map：：put()**函数是 PHP 中的内置函数，用于将键与值相关联。

**语法：**

```php
*void* public Ds\Map::put( $key, $value )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$key:** it is used to hold the key to associate values.
*   **$value:** is used to hold the value of key.

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Map：：Put()**函数：

**程序 1：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map();

$map->put("a", "Geeks");
$map->put("b", "for");
$map->put("c", "Geeks");

// Display output
print_r($map);

// Declare a new map
$map = new \Ds\Map();

$map->put("a", "Computer");
$map->put("b", "Science");
$map->put("c", "Portal");

// Display output
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
            [key] => a
            [value] => Computer
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => Science
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => Portal
        )

)

```

**程序 2：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map();

$map->put("Geeks1", "computer");
$map->put("Geeks2", "science");
$map->put("Geeks3", 5);
$map->put("Geeks3", 20);

// Display result
var_dump($map);

?>
```

**输出：**

```php
object(Ds\Map)#1 (3) {
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
    int(20)
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-map.put.php](https://www.php.net/manual/en/ds-map.put.php)