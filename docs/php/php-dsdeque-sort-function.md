# PHP|ds\Deque Sort()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-sort-function/](https://www.geeksforgeeks.org/php-dsdeque-sort-function/)

**Ds\Deque：：Sort()**函数是 PHP 中的一个内置函数，用于通过按升序排列元素来对 Deque 进行就地排序。

**语法：**

```php
*public* Ds\Deque::sort( $comparator ) : void
```

**参数：**：此函数接受单个参数*$compator*，该参数包含决定如何对元素进行排序的函数。 它有助于定制排序功能。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**Ds\Deque：：Sort()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([5, 6, 3, 2, 7, 1]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Use sort() function to sort
// the elements
$deck->sort();

echo("Sorted Deque\n");

// Display the Deque elements
print_r($deck);;

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
Sorted Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 5
    [4] => 6
    [5] => 7
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([5, 6, 3, 2, 7, 1]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// comparator to sort in reverse order
$deck->sort(function($first, $second) {
    return $first <= $second;
});

echo("Sorted Deque\n");

// Display the Deque elements
print_r($deck);;

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
Sorted Deque
Ds\Deque Object
(
    [0] => 7
    [1] => 6
    [2] => 5
    [3] => 3
    [4] => 2
    [5] => 1
)

```

**引用：**[http://php.net/manual/en/ds-deque.sort.php](http://php.net/manual/en/ds-deque.sort.php)