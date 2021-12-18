# PHP|ds\Deque Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-reverse-function/](https://www.geeksforgeeks.org/php-dsdeque-reverse-function/)

**Ds\Deque：：Reverse()**函数是 PHP 中的一个内置函数，用于就地反转 Deque 中的元素。

**语法：**

```php
*public* Ds\Deque::reverse( void ) : void
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\deque：：Reverse()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
var_dump($deck);

// Reversing the deque
$deck->reverse();

echo("\nElements of the reversed deque\n");

// Display the Deque elements
var_dump($deck);

?>
```

**输出：**

```php
Elements of Deque
object(Ds\Deque)#1 (6) {
  [0]=>
  int(10)
  [1]=>
  int(20)
  [2]=>
  int(30)
  [3]=>
  int(40)
  [4]=>
  int(50)
  [5]=>
  int(60)
}

Elements of the reversed deque
object(Ds\Deque)#1 (6) {
  [0]=>
  int(60)
  [1]=>
  int(50)
  [2]=>
  int(40)
  [3]=>
  int(30)
  [4]=>
  int(20)
  [5]=>
  int(10)
}

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "GFG", "ABC"]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Reversing the deque
$deck->reverse();

echo("\nElements of the reversed deque\n");

// Display the Deque elements
print_r($deck);

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => GFG
    [2] => ABC
)

Elements of the reversed deque
Ds\Deque Object
(
    [0] => ABC
    [1] => GFG
    [2] => geeks
)

```

**引用：**[http://php.net/manual/en/ds-deque.reverse.php](http://php.net/manual/en/ds-deque.reverse.php)