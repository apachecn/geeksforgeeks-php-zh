# PHP|ds\deeque sum()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-sum-function/](https://www.geeksforgeeks.org/php-dsdeque-sum-function/)

**Ds\Deque：：sum()**函数是 PHP 中的一个内置函数，用于返回 Deque 中存在的所有元素的总和。

**语法：**

```php
*public* Ds\Deque::sum( void ) : number
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回所有 Deque 元素的总和。

以下程序说明了 PHP 中的**ds\deque：：sum()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([5, 6, 3, 2, 7, 1]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("Sum of all Deque elements: ");

// Use sum() function to add all
// Deque elements
var_dump($deck->sum());

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 5
    [1] => 6
    [2] => 3
    [3] => 2
    [4] => 7
    [5] => 1
)
Sum of all Deque elements: int(24)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1.5, 6.3, 2.3, 7.2, 4.7, 9.3]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("Sum of all Deque elements: ");

// Use sum() function to add all
// Deque elements
var_dump($deck->sum());

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 1.5
    [1] => 6.3
    [2] => 2.3
    [3] => 7.2
    [4] => 4.7
    [5] => 9.3
)
Sum of all Deque elements: float(31.3)

```

**引用：**[http://php.net/manual/en/ds-deque.sum.php](http://php.net/manual/en/ds-deque.sum.php)