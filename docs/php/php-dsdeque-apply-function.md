# PHP|ds\Deque Apply()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-apply-function/](https://www.geeksforgeeks.org/php-dsdeque-apply-function/)

**Ds\Deque：：Apply()**函数是 PHP 中的一个内置函数，用于通过执行回调函数定义的操作来更新 Deque 的值。

**语法：**

```php
*public* Ds\Deque::apply( $callback ) : void

```

**参数：**此函数接受单个参数*$callback*，该参数保存定义要在 Deque 的每个元素上执行的操作的函数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\deque：：Apply()**函数：

**程序 1：**

```php
<?php

// Declare deque
$deck = new \Ds\Deque([1, 2, 3, 4, 5, 6]);

echo("\nElements in the deque are\n");

// Display the deque elements
print_r($deck);

// Use apply() function to implement
// the operation
$deck->apply(function($element) { 
    return $element * 10; 
});

echo("\nUpdated elements in the deque\n");

// Display the deque elements
print_r($deck);

?> 
```

**输出：**

```php
Elements in the deque are
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)

Updated elements in the deque
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

// Declare deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("\nElements in the deque are\n");

// Display the deque elements
print_r($deck);

// Use apply() function to implement
// the operation
$deck->apply(function($element) { 
    return $element % 10; 
});

echo("\nUpdated elements in the deque\n");

// Display the deque elements
print_r($deck);

?> 
```

**输出：**

```php
Elements in the deque are
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
)

Updated elements in the deque
Ds\Deque Object
(
    [0] => 0
    [1] => 0
    [2] => 0
    [3] => 0
    [4] => 0
    [5] => 0
)

```

**引用：**[http://php.net/manual/en/ds-deque.apply.php](http://php.net/manual/en/ds-deque.apply.php)