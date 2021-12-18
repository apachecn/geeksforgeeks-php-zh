# PHP|ds\Deque Sorted()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-sorted-function/](https://www.geeksforgeeks.org/php-dsdeque-sorted-function/)

**Ds\Deque：：Sorted()**函数是 PHP 中的一个内置函数，用于返回 Deque 的副本，该副本包含原始 Deque 中的元素(按升序排列)。

**语法：**

```php
*public* Ds\Deque::sorted( $comparator ) : Ds\Deque
```

**参数：**此函数接受单个参数*$compator*，该参数保存用于对 Deque 进行排序的比较器函数。

**返回值：**此函数返回一个 Deque，该 Deque 按排序顺序包含原始 Deque 的元素。

下面的程序说明了 PHP 中的**ds\deque：：sorted()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([4, 5, 3, 2, 8, 1, 9]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("Sorted Deque\n");

// Use sorted() function to 
// sort Deque elements
print_r($deck->sorted());

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 4
    [1] => 5
    [2] => 3
    [3] => 2
    [4] => 8
    [5] => 1
    [6] => 9
)
Sorted Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 8
    [6] => 9
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([4, 5, 3, 2, 8, 1, 9]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Use comparator function to sort elements
$deck = $deck->sorted(function($var1, $var2) {
    return $var1 <= $var2;
});

echo("Sorted Deque\n");

// Use sorted() function to 
// sort Deque elements
print_r($deck);

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 4
    [1] => 5
    [2] => 3
    [3] => 2
    [4] => 8
    [5] => 1
    [6] => 9
)
Sorted Deque
Ds\Deque Object
(
    [0] => 9
    [1] => 8
    [2] => 5
    [3] => 4
    [4] => 3
    [5] => 2
    [6] => 1
)

```

**引用：**[http://php.net/manual/en/ds-deque.sorted.php](http://php.net/manual/en/ds-deque.sorted.php)