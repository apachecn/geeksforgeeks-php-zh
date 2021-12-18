# PHP|ds\Deque isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-isempty-function/](https://www.geeksforgeeks.org/php-dsdeque-isempty-function/)

**ds\Deque：：isEmpty()**函数是 PHP 中的内置函数，用于检查 Deque 是否为空。

**语法：**

```
*public* Ds\Deque::isEmpty( void ) : bool

```

**参数：**此函数不接受任何参数。

**返回值：**如果 Deque 为空，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**ds\deque：：isEmpty()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Original Deque\n");

// Display the Deque elements
print_r($deck);

// Use isEmpty() function to check
// the deque is empty or not
var_dump($deck->isEmpty());

?>
```

**输出：**

```
Original Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
bool(false)

```

**程序 2：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Original Deque\n");

// Display the Deque elements
print_r($deck);

// Clearing the Deque
$deck->clear();

// Use isEmpty() function to check
// the deque is empty or not
var_dump($deck->isEmpty());

?>
```

**输出：**

```
Original Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
bool(true)

```

**引用：**[http://php.net/manual/en/ds-deque.isempty.php](http://php.net/manual/en/ds-deque.isempty.php)