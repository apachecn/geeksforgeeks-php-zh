# PHP|ds\Deque CONTAINS()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-contains-function/](https://www.geeksforgeeks.org/php-dsdeque-contains-function/)

DS\Deque：：CONTAINS()函数是 PHP 中的一个内置函数，用于检查元素是否存在于 Deque 中。

**语法：**

```php
*public* Ds\Deque::contains( $values ) : bool

```

**参数：**此函数接受单个或多个值，这些值需要检查序列中是否存在值。

**返回值：**如果元素存在于 Deque 中，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 DS\Deque：：CONTAINS()函数：

**程序 1：**

```php
<?php

// Declare deque of default size
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the deque\n");

// Display the deque elements
var_dump($deck);

echo("\nChecking for the element in the deque\n");

// Use contains() function to check 3 is
// present in the deque or not
var_dump($deck->contains(3));

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

Checking for the element in the deque
bool(true)

```

**程序 2：**

```php
<?php

// Declare deque of default size
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements in the deque\n");

// Display the deque elements
var_dump($deck);

echo("\nChecking for the element in the deque\n");

// Use contains() function to check 3 is
// present in the deque or not
var_dump($deck->contains("GFG"));

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

Checking for the element in the deque
bool(false)

```

**引用：**[http://php.net/manual/en/ds-deque.contains.php](http://php.net/manual/en/ds-deque.contains.php)