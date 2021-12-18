# PHP|ds\Deque Allocation()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-allocate-function/](https://www.geeksforgeeks.org/php-dsdeque-allocate-function/)

**Ds\Deque：：Allocation()**函数是 PHP 中的一个内置函数，用于按照参数中指定的方式分配内存。 如果未定义该参数，则将创建默认大小的 Deque。

**语法：**

```php
*public* Ds\Deque::allocate( $capacity ) : void

```

**参数：**此函数接受单个参数*$acity*，该参数保存要为其分配空间的值的数量。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 DS\Deque：：Allocation()函数：

**程序 1：**

```php
<?php

// Declare Deque of default size
$deq = new \Ds\Deque();

// Display the capacity of Deque
var_dump($deq->capacity());

// Allocating space for 50 values
// to the Deque
$deq->allocate(50);

// Display the capacity of Deque
var_dump($deq->capacity());

?> 
```

**输出：**

```php
int(8)
int(64)

```

**程序 2：**

```php
<?php

// Declare Deque of default size
$deck = new \Ds\Deque();

// Display the Deque capacity
var_dump($deck->capacity());

// Allocating space for 50 values
// to the Deque
$deck->allocate(50);

// Display the Deque capacity
var_dump($deck->capacity());

// Allocating space for 60 values
// to the Deque
$deck->allocate(60);

// Display the Deque capacity
var_dump($deck->capacity());

?>
```

**输出：**

```php
int(8)
int(64)
int(64)

```

**引用：**[http://php.net/manual/en/ds-deque.allocate.php](http://php.net/manual/en/ds-deque.allocate.php)