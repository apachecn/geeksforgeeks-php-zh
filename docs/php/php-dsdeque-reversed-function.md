# PHP|ds\Deque Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-reversed-function/](https://www.geeksforgeeks.org/php-dsdeque-reversed-function/)

**Ds\Deque：：Reverse()**函数是 PHP 中的一个内置函数，用于返回包含颠倒顺序的元素的 Deque 副本。

**语法：**

```
*public* Ds\Deque::reversed( void ) : Ds\Deque
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个 Deque，它是包含逆序元素的原始 Deque 的副本。

下面的程序说明了 PHP 中的**Ds\deque：：Reverse()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
var_dump($deck);

// Reversing the deque
$deck_new = $deck->reversed();

echo("\nElements of the reversed deque\n");

// Display the Deque elements
var_dump($deck_new);

?>
```

**输出：**

```
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
object(Ds\Deque)#2 (6) {
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

```
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks", "articles"]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Reversing the deque
$deck_new = $deck->reversed();

echo("\nElements of the reversed deque\n");

// Display the Deque elements
print_r($deck_new);

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
    [3] => articles
)

Elements of the reversed deque
Ds\Deque Object
(
    [0] => articles
    [1] => geeks
    [2] => for
    [3] => geeks
)

```

**引用：**[http://php.net/manual/en/ds-deque.reversed.php](http://php.net/manual/en/ds-deque.reversed.php)