# PHP|ds\set filter()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-filter-function/](https://www.geeksforgeeks.org/php-dsset-filter-function/)

**ds\set：：filter()**函数是 PHP 中的一个内置函数，用于使用 Filter 函数创建新的集合。

**语法：**

```php
*Ds\Set* public Ds\Set::filter( $callback )
```

**参数：**此函数接受单个参数**$callback**，该参数是可选的，如果应该包含该值，则返回 True，否则返回 False。

**返回值：**此函数返回一个新的集合，其中包含回调返回 True 的所有值，如果未提供回调，则包含转换为 True 的所有值。

以下程序说明了 PHP 中的**ds\set：：filter()**函数：

**程序 1：**

```php
<?php 

// Create new set 
$set = new \Ds\Set([10, 20, 30, 40, 50]); 

// Display new set using filter function 
var_dump($set->filter(function($val) { 
    return $val % 4 == 0; 
})); 

?> 
```

**输出：**

```php
object(Ds\Set)#3 (2) {
  [0]=>
  int(20)
  [1]=>
  int(40)
}

```

**程序 2：**

```php
<?php 

// Create new set
$set = new \Ds\Set([2, 5, 4, 8, 3, 9]); 

// Display new set using filter function 
var_dump($set->filter(function($val) { 
    return $val; 
})); 

?> 
```

**输出：**

```php
object(Ds\Set)#3 (6) {
  [0]=>
  int(2)
  [1]=>
  int(5)
  [2]=>
  int(4)
  [3]=>
  int(8)
  [4]=>
  int(3)
  [5]=>
  int(9)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.filter.php](https://www.php.net/manual/en/ds-set.filter.php)