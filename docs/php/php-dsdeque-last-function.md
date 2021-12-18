# PHP|ds\Deque last()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-last-function/](https://www.geeksforgeeks.org/php-dsdeque-last-function/)

**Ds\Deque：：last()**函数是 PHP 中的一个内置函数，用于在 Deque 不为空的情况下返回 Deque 的最后一个元素。

**语法：**

```php
*public* Ds\Deque::last( void ) : mixed
```

**参数：**此函数不接受任何参数。

**返回值：**如果双队列中的最后一个元素不为空，则此函数返回该元素。

**异常：**如果 Deque 为空，则此函数抛出*UnderflowException*。

以下程序说明了 PHP 中的**ds\deque：：last()**函数：

**程序 1：**

```php
<?php

// Create a Deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the deque\n");

// Display the Deque Elements
var_dump($deck);

echo("\nLast element in the deque: ");

// Use last() function to display the 
// last element from the deque
var_dump($deck->last());

?>
```

**输出：**

```php
Elements in the deque
object(Ds\Deque)#1 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}

Last element in the deque: int(6)

```

**程序 2：**

```php
<?php

// Create a Deque
$deck = new \Ds\Deque(["geeks", "for", "geeks"]);

echo("Elements in the deque\n");

// Display the Deque Elements
print_r($deck);

echo("\nLast element in the deque: ");

// Use last() function to display the 
// last element from the deque
print_r($deck->last());

?>
```

**输出：**

```php
Elements in the deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

Last element in the deque: geeks

```

**引用：**[http://php.net/manual/en/ds-deque.last.php](http://php.net/manual/en/ds-deque.last.php)