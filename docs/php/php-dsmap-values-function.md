# PHP|ds\Map Values()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-values-function/](https://www.geeksforgeeks.org/php-dsmap-values-function/)

**ds\Map：：Values()**函数是 PHP 中的一个内置函数，用于返回一系列映射值。

**语法：**

```php
*Ds\Sequence* public Ds\Map::values ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**它返回一个包含映射所有值的 Ds\Sequence。

以下程序说明了 PHP 中的**ds\Map：：Values()**函数：

**程序 1：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map(["a" => "Geeks", "b" => "for",
                                   "c" => "Geeks"]); 

print_r($map->values());

// Declare another new map
$map = new \Ds\Map(["b" => "Computer", "e" => 
                       "Science", "f" => "Portal"]); 

print_r($map->values());

?>
```

**输出：**

```php
Ds\Vector Object
(
    [0] => Geeks
    [1] => for
    [2] => Geeks
)
Ds\Vector Object
(
    [0] => Computer
    [1] => Science
    [2] => Portal
)

```

**程序 2：**

```php
<?php 

// Declare a new map
$map = new \Ds\Map(["Geeks1" => "computer", 
 "Geeks2" => "science", "Geeks3" => 5, "Geeks4" => 20]); 

var_dump($map->values());

// Declare another new map
$map = new \Ds\Map(["x" => "A", "y" => "B", "z" => "C"]); 

var_dump($map->values());

?>
```

**输出：**

```php
object(Ds\Vector)#2 (4) {
  [0]=>
  string(8) "computer"
  [1]=>
  string(7) "science"
  [2]=>
  int(5)
  [3]=>
  int(20)
}
object(Ds\Vector)#1 (3) {
  [0]=>
  string(1) "A"
  [1]=>
  string(1) "B"
  [2]=>
  string(1) "C"
}

```

**引用：**[https://www.php.net/manual/en/ds-map.values.php](https://www.php.net/manual/en/ds-map.values.php)