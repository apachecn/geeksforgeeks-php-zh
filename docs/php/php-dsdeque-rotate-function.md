# PHP|ds\Deque Rotate()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-rotate-function/](https://www.geeksforgeeks.org/php-dsdeque-rotate-function/)

**Ds\Deque：：Rotate()**函数是 PHP 中的一个内置函数，用于将 Deque 的元素旋转给定的旋转次数。

**语法：**

```
*public* Ds\Deque::rotate( $rotations ) : void
```

**参数：**此函数接受单个参数*$rotation*，该参数保存要旋转的 Deque 中元素的旋转次数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**Ds\Deque：：Rotate()**函数：

**程序 1：**

```
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

// Rotating the deque by 2 positions
$deck->rotate(2);

echo("Rotated Deque\n");

// Display the Deque elements
print_r($deck);

?>
```

**输出：**

```
Elements of Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
Rotated Deque
Ds\Deque Object
(
    [0] => 3
    [1] => 4
    [2] => 5
    [3] => 6
    [4] => 1
    [5] => 2
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

// Rotating the deque by 2 positions
$deck->rotate(2);

echo("Rotated Deque\n");

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
Rotated Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => practice
    [2] => geeks
    [3] => for
)

```

**引用：**[http://php.net/manual/en/ds-deque.rotate.php](http://php.net/manual/en/ds-deque.rotate.php)