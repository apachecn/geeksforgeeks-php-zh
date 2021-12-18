# PHP|ds\Map filter()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-filter-function/](https://www.geeksforgeeks.org/php-dsmap-filter-function/)

**ds\Map：：Filter()**函数是 PHP 中的内置函数，用于使用 Filter 函数创建新映射。

**语法：**

```php
*Ds\Map* public Ds\Map::filter( $callback )
```

**参数：**它包含单个参数**$callback**，这是一个可选参数，如果应该包含该值，则返回 True，否则返回 False。

**返回值：**此函数返回一个新映射，其中包含回调返回 True 的所有对，如果未提供回调，则包含转换为 True 的所有值。

以下程序说明了 PHP 中的**ds\Map：：Filter()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the filter() 
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map([
    1 => "Welcome",
    2 => "to",
    3 => "Geeks",  
    4 => "for",
    5 => "Geeks"]);

// Display new sequence using filter function 
var_dump($map->filter(function($key, $val) { 
    return $key % 3 == 0; 
})); 

?> 
```

**输出：**

```php
object(Ds\Map)#3 (1) {
  [0]=>
  object(Ds\Pair)#2 (2) {
    ["key"]=>
    int(3)
    ["value"]=>
    string(5) "Geeks"
  }
}

```

**程序 2：**

```php
<?php 
// PHP program to illustrate the filter() 
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map([
        1 => 10, 
        2 => 20,
        3 => 30, 
        4 => 40,
        5 => 50]); 

// Display new sequence using filter function 
var_dump($map->filter(function($key, $val) { 
    return $val % 20 == 0; 
})); 

?> 
```

**输出：**

```php
object(Ds\Map)#3 (2) {
  [0]=>
  object(Ds\Pair)#2 (2) {
    ["key"]=>
    int(2)
    ["value"]=>
    int(20)
  }
  [1]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    int(4)
    ["value"]=>
    int(40)
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-map.filter.php](https://www.php.net/manual/en/ds-map.filter.php)