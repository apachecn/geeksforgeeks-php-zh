# PHP|ds\Deque POP()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-pop-function/](https://www.geeksforgeeks.org/php-dsdeque-pop-function/)

**Ds\Deque：：op()**函数是 PHP 中的一个内置函数，用于从 Deque 中删除最后一个元素(如果 Deque 不为空)并返回它。 如果 Deque 为空，则抛出异常。

**语法：**

```
*public* Ds\Deque::pop( void ) : mixed
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回从 Deque 中删除的最后一个元素。

以下程序说明了 PHP 中的**ds\deque：：op()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// last element in the deque
echo("\nLast element of deque: ");

// Use pop() function to removing last
// element from Deque and Display it
print_r($deck->pop());

echo("\nElements of Deque\n");

// Display the Deque elements
print_r($deck);

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

Last element of deque: 60
Elements of Deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
)

```

**程序 2：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks", "practice"]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// last element in the deque
echo("\nLast element of deque: ");

// Use pop() function to removing last
// element from Deque and Display it
print_r($deck->pop());

echo("\nElements of Deque\n");

// Display the Deque elements
print_r($deck);

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
    [3] => practice
)

Last element of deque: practice
Elements of Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

```

**引用：**[http://php.net/manual/en/ds-deque.pop.php](http://php.net/manual/en/ds-deque.pop.php)