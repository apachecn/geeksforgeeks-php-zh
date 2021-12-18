# PHP|ds\Deque get()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-get-function/](https://www.geeksforgeeks.org/php-dsdeque-get-function/)

**ds\deque：：get()**函数是 PHP 中的一个内置函数，用于返回给定索引处的值。

**语法：**

```php
*public* Ds\Deque::get( $index ) : mixed

```

**参数：**此函数接受单个参数*$index*，该参数保存要找到的元素的索引。

**返回值：**此函数返回给定索引处的值。

下面的程序说明了 PHP 中的**Ds\Deque：：Get()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 3, 40, 50, 6]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nElement at index 2 in the deque: ");

// Use get() function to find the index value
var_dump($deck->get(2));

?>
```

**输出：**

```php
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

Element at index 2 in the deque: int(3)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for", "geeks", "PHP"]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nElement at index 2 in the deque: ");

// Use get() function to find the index value
var_dump($deck->get(2));

?>
```

**输出：**

```php
Elements in the Deque
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
    [3] => PHP
)

Element at index 2 in the deque: string(5) "geeks"

```

**引用：**[http://php.net/manual/en/ds-deque.get.php](http://php.net/manual/en/ds-deque.get.php)