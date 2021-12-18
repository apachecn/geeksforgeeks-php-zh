# PHP|ds\deeque first()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-first-function/](https://www.geeksforgeeks.org/php-dsdeque-first-function/)

**Ds\Deque：：First()**函数是 PHP 中的一个内置函数，如果 Deque 不为空，它将返回 Deque 中的第一个值。

**语法：**

```
*public* Ds\Deque::first( void ) : mixed

```

**参数：**此函数不接受任何参数。

**返回值：**如果 Deque 不为空，则此函数返回 Deque 中的第一个元素。

下面的程序说明了 PHP 中的**Ds\Deque：：First()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 3, 40, 50, 6]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nFirst element in the deque: ");

// Use first() function to find
// first element in the deque
var_dump($deck->first());

?>
```

**输出：**

```
Elements in the Deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 3
    [3] => 40
    [4] => 50
    [5] => 6
)

First element in the deque: int(10)

```

**程序 2：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque(["Geeks", "for", "GFG"]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nFirst element in the deque: ");

// Use first() function to find
// first element in the deque
var_dump($deck->first());

?>
```

**输出：**

```
Elements in the Deque
Ds\Deque Object
(
    [0] => Geeks
    [1] => for
    [2] => GFG
)

First element in the deque: string(5) "Geeks"

```

**引用：**[http://php.net/manual/en/ds-deque.first.php](http://php.net/manual/en/ds-deque.first.php)