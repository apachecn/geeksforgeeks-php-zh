# PHP|ds\set clear()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-clear-function/](https://www.geeksforgeeks.org/php-dsset-clear-function/)

**ds\set：：clear()**函数是 PHP 中的一个内置函数，用于从集合中删除所有值。

**语法：**

```
*void* public Ds\Set::clear( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\set：：clear()**函数：

**程序 1：**

```
<?php 

// Declare new Set
$set = new \Ds\Set([1, 2, 3, 4, 5, 6]); 

// Display the Set element 
print_r($set); 

// Use clear() function to remove elements 
$set->clear(); 

// Display the Set element 
print_r($set); 

?> 
```

**输出：**

```
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
Ds\Set Object
(
)

```

**程序 2：**

```
<?php 

// Declare new Set
$set = new \Ds\Set([10, 15, 21, 13, 16, 18]); 

// Display the Set element 
var_dump($set); 

// Use clear() function to remove elements 
$set->clear(); 

// Display the Set element 
var_dump($set); 

?> 
```

**输出：**

```
object(Ds\Set)#1 (6) {
  [0]=>
  int(10)
  [1]=>
  int(15)
  [2]=>
  int(21)
  [3]=>
  int(13)
  [4]=>
  int(16)
  [5]=>
  int(18)
}
object(Ds\Set)#1 (0) {
}

```

**引用：**[http://php.net/manual/en/ds-set.clear.php](http://php.net/manual/en/ds-set.clear.php)