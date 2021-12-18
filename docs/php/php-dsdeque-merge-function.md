# PHP|ds\Deque Merge()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-merge-function/](https://www.geeksforgeeks.org/php-dsdeque-merge-function/)

**Ds\Deque：：Merge()**函数是 PHP 中的一个内置函数，用于在将一个 Deque 的所有元素与另一个 Deque 的所有元素合并后，通过将所有值添加到一个副本中来返回合并后的 Deque，并返回该副本。

**语法：**

```
*public* Ds\Deque::merge( $values ) : Ds\Deque
```

**参数：**此函数接受单个参数*$values*，该参数包含要与调用 Deque 合并的值。

**返回值：**此函数返回一个 Deque，其中包含两个 Deque 的所有元素。

下面的程序说明了 PHP 中的**ds\deque：：merge()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of first deque\n");

// Display the deque Elements
print_r($deck);

// Declare another deque
$deck2 = new \Ds\Deque([70, 80, 90, 100]);

echo("\nElements of second deque\n");
print_r($deck2);

echo("\nMerged deque elements\n");

// Merge the both deque
print_r($deck->merge($deck2));

?>
```

**输出：**

```
Elements of first deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
)

Elements of second deque
Ds\Deque Object
(
    [0] => 70
    [1] => 80
    [2] => 90
    [3] => 100
)

Merged deque elements
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
    [6] => 70
    [7] => 80
    [8] => 90
    [9] => 100
)

```

**程序 2：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks"]);

echo("Elements of first deque\n");

// Display the deque Elements
print_r($deck);

// Declare another deque
$deck2 = new \Ds\Deque(["practicing", "data", "structures"]);

echo("\nElements of second deque\n");
print_r($deck2);

echo("\nMerged deque elements\n");

// Merge the both deque
print_r($deck->merge($deck2));

?>
```

**输出：**

```
Elements of first deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

Elements of second deque
Ds\Deque Object
(
    [0] => practicing
    [1] => data
    [2] => structures
)

Merged deque elements
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
    [3] => practicing
    [4] => data
    [5] => structures
)

```

**引用：**[http://php.net/manual/en/ds-deque.merge.php](http://php.net/manual/en/ds-deque.merge.php)