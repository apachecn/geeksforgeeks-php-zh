# PHP|ds\Deque count()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-count-function/](https://www.geeksforgeeks.org/php-dsdeque-count-function/)

**Ds\Deque：：Count()**函数是 PHP 中的一个内置函数，用于获取 Deque 中的元素数量。

**语法：**

```php
*public* Ds\Deque::count( void ) : int

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回队列中的元素数。

以下程序说明了 PHP 中的**ds\deque：：count()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nNumber of elements in the Deque: ");

print_r($deck->count());

?>
```

**输出：**

```php
Elements in the Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

Number of elements in the Deque: 6

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks"]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nNumber of elements in the Deque: ");

print_r($deck->count());

?>
```

**输出：**

```php
Elements in the Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

Number of elements in the Deque: 3

```

**引用：**[http://php.net/manual/en/ds-deque.count.php](http://php.net/manual/en/ds-deque.count.php)