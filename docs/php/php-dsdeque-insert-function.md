# PHP|ds\Deque Insert()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-insert-function/](https://www.geeksforgeeks.org/php-dsdeque-insert-function/)

**Ds\Deque：：Insert()**函数是 PHP 中的一个内置函数，用于在 Deque 中的给定索引处插入值。

**语法：**

```php
*public* Ds\Deque::insert( $index, $values ) : void

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$index:** this parameter holds the index of the element to be inserted.
*   **$value:** this parameter holds the value to be inserted into the given index in Deque.

**返回值：**此函数不返回任何值。

**异常：**如果 Deque 为空，则此函数抛出*OutOfRangeException*。

下面的程序说明了 PHP 中的**Ds\Deque：：Insert()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nInsert 10 at index 4 in the deque\n");

// Use insert() function to inserting
// element in the deque at index 4
$deck->insert(4, 10);

// Display the Deque elements
print_r($deck);

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

Insert 10 at index 4 in the deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 10
    [5] => 5
    [6] => 6
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Original Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nModified Deque\n");

// Use insert() function to inserting
// element in the deque at index 4
$deck->insert(3, ...[10, 20, 30, 40]);

// Display the Deque elements
print_r($deck);

?>
```

**输出：**

```php
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

Modified Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 10
    [4] => 20
    [5] => 30
    [6] => 40
    [7] => 4
    [8] => 5
    [9] => 6
)

```

**引用：**[http://php.net/manual/en/ds-deque.insert.php](http://php.net/manual/en/ds-deque.insert.php)