# PHP|ds\Deque Remove()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-remove-function/](https://www.geeksforgeeks.org/php-dsdeque-remove-function/)

**Ds\Deque：：Remove()**函数是 PHP 中的一个内置函数，用于删除和返回索引值。

**语法：**

```
*public* Ds\Deque::remove( $index ) : mixed
```

**参数：**此函数接受单个参数*$index*，该参数保存要返回和删除元素的 Deque 的索引。

**返回值：**此函数返回并移除 Deque 中给定索引处的元素。

下面的程序说明了 PHP 中的**Ds\Deque：：Remove()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nElement at index 2: ");

// Use remove() function to remove the
// element at index 2 and return it
print_r($deck->remove(2));

?>
```

**输出：**

```
Elements of Deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
)

Element at index 2: 30

```

**程序 2：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks"]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nElement at index 1: ");

// Use remove() function to remove the
// element at index 2 and return it
print_r($deck->remove(1));

?>
```

**输出：**

```
Elements of Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

Element at index 1: for

```

**引用：**[http://php.net/manual/en/ds-deque.remove.php](http://php.net/manual/en/ds-deque.remove.php)