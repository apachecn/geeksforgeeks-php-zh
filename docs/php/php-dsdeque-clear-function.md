# PHP|ds\Deque Clear()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-clear-function/](https://www.geeksforgeeks.org/php-dsdeque-clear-function/)

**Ds\Deque：：Clear()**函数是 PHP 中的一个内置函数，用于通过从 Deque 中删除所有元素来清除 Deque。

**语法：**

```
*public* Ds\Deque::clear( void ) : void

```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**Ds\Deque：：Clear()**函数：

**程序 1：**

```
<?php

// Declare deque of default size
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the deck:\n");

// Display the Deque elements
print_r($deck);

// Use clear() function to clear the deque
$deck->clear();

// Display the deque
print_r($deck);

?> 
```

**输出：**

```
Elements in the deck:
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
Ds\Deque Object
(
)

```

**程序 2：**

```
<?php

// Declare deque of default size
$deck = new \Ds\Deque(["geeks", "for", "geeks"]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

// Use clear() function to clear the deque
$deck->clear();

echo("Alter clearing the elements\n");
// Display the deque
print_r($deck);

?> 
```

**输出：**

```
Elements in the Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)
Alter clearing the elements
Ds\Deque Object
(
)

```

**引用：**[http://php.net/manual/en/ds-deque.clear.php](http://php.net/manual/en/ds-deque.clear.php)