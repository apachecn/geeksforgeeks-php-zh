# PHP|ds\Deque toArray()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-toarray-function/](https://www.geeksforgeeks.org/php-dsdeque-toarray-function/)

**ds\Deque：：toArray()**函数是 PHP 中的内置函数，用于将 Deque 转换为数组。 数组元素的顺序将与它们在 Deque 中的顺序相同。

**语法：**

```php
*public* Ds\Deque::toArray( void ) : array
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回以相同顺序包含 Deque 的所有元素的数组。

以下程序说明了 PHP 中的**ds\deque：：toArray()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([5, 6, 3, 2, 7, 1]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("Array elements\n");

// Use toArray() function to
// convert Deque into array
print_r($deck->toArray());

?>
```

**输出：**

```php
Elements of Deque
Ds\Deque Object
(
    [0] => 5
    [1] => 6
    [2] => 3
    [3] => 2
    [4] => 7
    [5] => 1
)
Array elements
Array
(
    [0] => 5
    [1] => 6
    [2] => 3
    [3] => 2
    [4] => 7
    [5] => 1
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["geeks", "for",
            "geeks", "data structures"]);

echo("Elements of Deque\n");

// Display the Deque elements
var_dump($deck);

echo("Array elements\n");

// Use toArray() function to
// convert Deque into array
var_dump($deck->toArray());

?>
```

**输出：**

```php
Elements of Deque
object(Ds\Deque)#1 (4) {
  [0]=>
  string(5) "geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "geeks"
  [3]=>
  string(15) "data structures"
}
Array elements
array(4) {
  [0]=>
  string(5) "geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "geeks"
  [3]=>
  string(15) "data structures"
}

```

**引用：**[http://php.net/manual/en/ds-deque.toarray.php](http://php.net/manual/en/ds-deque.toarray.php)