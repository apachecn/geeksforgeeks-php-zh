# PHP|ds\Deque Join()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-join-function/](https://www.geeksforgeeks.org/php-dsdeque-join-function/)

**Ds\Deque：：Join()**函数是 PHP 中的一个内置函数，用于将 Deque 中的所有值连接为一个字符串。 分隔符也可用于连接元素。

**语法：**

```php
*public* Ds\Deque::join( $glue ) : string

```

**参数：**此函数接受单个参数*$glue*，该参数保存分隔 Deque 元素的分隔符。

**返回值：**此函数返回作为字符串联接的 Deque 的所有值。

下面的程序说明了 PHP 中的**Ds\Deque：：Join()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Original Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nString form: ");

// Use join() function to joining
// the values in Deque
var_dump($deck->join("|"));

?>
```

**输出：**

```php
Original Deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

String form: string(11) "1|2|3|4|5|6"

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["Geeks", "for", "Geeks"]);

echo("Original Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nString form: ");

// Use join() function to joining
// the values in Deque
var_dump($deck->join());

?>
```

**输出：**

```php
Original Deque
Ds\Deque Object
(
    [0] => Geeks
    [1] => for
    [2] => Geeks
)

String form: string(13) "GeeksforGeeks"

```

**引用：**[http://php.net/manual/en/ds-deque.join.php](http://php.net/manual/en/ds-deque.join.php)