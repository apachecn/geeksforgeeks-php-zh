# PHP|ds\Deque Slice()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-slice-function/](https://www.geeksforgeeks.org/php-dsdeque-slice-function/)

**Ds\Deque：：Slice()**函数是 PHP 中的一个内置函数，用于返回子 Deque，其中包含索引范围内的 Deque 元素。

**语法：**

```php
*public* Ds\Deque::slice( $index, $length ) : Ds\Deque
```

**参数：**此函数接受上述两个参数，如下所述：

*   **index:** this parameter holds the starting index of the Sub Deque. The indicator value can be positive or negative. If the index value is positive, it starts with the index of Deque, and if the index value is negative, Deque starts with Ends.
*   **length:** this parameter saves the length of the subqueue. This parameter can take positive and negative values. If Length is positive, the subqueue size is equal to the given length, and if the length is negative, Deque stops so many values from the end.

**返回值：**此函数返回子队列，其中包含给定范围的队列中的切片元素。

下面的程序说明了 PHP 中的**Ds\Deque：：Slice()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Slicing deque from 2 to 5
$deck_new = $deck->slice(2, 5);

echo("\nDeque after slicing:\n");

// Display the Deque elements
print_r($deck_new);

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

Deque after slicing:
Ds\Deque Object
(
    [0] => 3
    [1] => 4
    [2] => 5
    [3] => 6
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Slicing deque from 3 to -2
$deck_new = $deck->slice(3, -2);

echo("\nDeque after slicing:\n");

// Display the Deque elements
print_r($deck_new);

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

Deque after slicing:
Ds\Deque Object
(
    [0] => 4
)

```

**引用：**[http://php.net/manual/en/ds-deque.slice.php](http://php.net/manual/en/ds-deque.slice.php)