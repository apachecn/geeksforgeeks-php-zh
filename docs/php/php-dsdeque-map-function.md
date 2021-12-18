# PHP|ds\deeque map()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-map-function/](https://www.geeksforgeeks.org/php-dsdeque-map-function/)

**ds\deque：：map()**函数是 PHP 中的一个内置函数，用于返回 Deque，其中每个元素都根据根据回调函数执行的操作进行了修改。

**语法：**

```php
*public* Ds\Deque::map( $callback ) : Ds\Deque
```

**参数：**此函数接受单个参数*$callback*，该参数包含要在 Deque 的每个元素上执行的操作的可调用函数。

**返回值：**此函数返回一个修改了每个元素的 Deque。

以下程序说明了 PHP 中的**ds\deque：：map()**函数：

**程序 1：**

```php
<?php

// Declare a Deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("Elements of deque\n");

// Display the Elements of Deque
print_r($deck);

// Deque after mapping each value as 
// per in the callable function
print_r($deck->map(function($element) {

    // performing operation on each element
    return $element * 10;
}));

?>
```

**输出：**

```php
Elements of deque
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
)

```

**程序 2：**

```php
<?php

// Declare a Deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of deque\n");

// Display the Elements of Deque
print_r($deck);

// Deque after mapping each value as 
// per in the callable function
print_r($deck->map(function($element) {

    // performing operation on each element
    return $element / 10;
}));

?>
```

**输出：**

```php
Elements of deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
)
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

```

**引用：**[http://php.net/manual/en/ds-deque.map.php](http://php.net/manual/en/ds-deque.map.php)