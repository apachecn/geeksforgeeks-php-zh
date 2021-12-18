# PHP|ds\Deque Capacity()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-capacity-function/](https://www.geeksforgeeks.org/php-dsdeque-capacity-function/)

**ds\Deque：：Capacity()**函数是 PHP 中的一个内置函数，用于获取 Deque 的当前容量。

**语法：**

```php
*public* Ds\Deque::capacity( void ) : int

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Deque 的当前容量。

以下程序说明了 PHP 中的**Ds\Deque：：Capacity()**函数：

**程序 1：**

```php
<?php

// Allocating deque of default size
$deck = new \Ds\Deque();

echo("Default size of Deque: ");

// Display the current capacity of the deque
var_dump($deck->capacity());

// Allocating space for 50 values to the deque
$deck->allocate(50);

echo("Allocated size of Deque: ");

// Display the current capacity of the deque
var_dump($deck->capacity());

?> 
```

**输出：**

```php
Default size of Deque: int(8)
Allocated size of Deque: int(64)

```

**程序 2：**

```php
<?php

// Declare Deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements of Deque\n");

// Display the Deque elements
var_dump($deck);

echo("\nCapacity of Deque: ");

// Display the capacity of Deque
var_dump($deck->capacity());

?>
```

**输出：**

```php
Elements of Deque
object(Ds\Deque)#1 (6) {
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

Capacity of Deque: int(8)

```

**引用：**[http://php.net/manual/en/ds-deque.capacity.php](http://php.net/manual/en/ds-deque.capacity.php)