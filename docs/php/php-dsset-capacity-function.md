# PHP|ds\set acity()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-capacity-function/](https://www.geeksforgeeks.org/php-dsset-capacity-function/)

**ds\set：：Capacity()**函数是 PHP 中的内置函数，用于返回集合的容量。

**语法：**

```php
*int* public Ds\Set::capacity( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 SET 的当前容量。

以下程序说明了 PHP 中的**ds\set：：Capacity()**函数：

**程序 1：**

```php
<?php 

// Declare an empty set 
$set = new \Ds\Set();

echo("Default size of Set: "); 

// Display the current capacity
var_dump($set->capacity()); 

// Allocating space for 50 values
$set->allocate(50); 

echo("Allocated size of Set: "); 

// Display the current capacity
var_dump($set->capacity()); 

?> 
```

**输出：**

```php
Default size of Set: int(8)
Allocated size of Set: int(64)

```

**程序 2：**

```php
<?php 

// Declare a set
$set = new \Ds\Set([1, 2, 3, 4, 5, 6]); 

echo("Elements of Set\n"); 

// Display the Set elements 
var_dump($set); 

echo("\nCapacity of Set: "); 

// Display the capacity of Set 
var_dump($set->capacity()); 

?> 
```

**输出：**

```php
Elements of Set
object(Ds\Set)#1 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}

Capacity of Set: int(8)

```

**引用：**[http://php.net/manual/en/ds-set.capacity.php](http://php.net/manual/en/ds-set.capacity.php)