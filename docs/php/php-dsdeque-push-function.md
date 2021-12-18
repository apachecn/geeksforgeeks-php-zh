# PHP|ds\Deque Push()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-push-function/](https://www.geeksforgeeks.org/php-dsdeque-push-function/)

**Ds\Deque：：Push()**函数是 PHP 中的一个内置函数，用于通过在 Deque 末尾追加一个元素来将元素添加到 Deque。

**语法：**

```php
*public* Ds\Deque::push( $values ) : void
```

**参数：**此函数接受单个参数*$values*，该参数保存要添加到 Deque 的元素。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**Ds\Deque：：Push()**函数：

**程序 1：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nAdding 70 in the deque\n");

// Use push() function to add elements
$deck->push(70);

echo("\nElements of Deque\n");

// Display the Deque elements
print_r($deck);

?>
```

**输出：**

```php
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

Adding 70 in the deque

Elements of Deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
    [6] => 70
)

```

**程序 2：**

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 30, 40, 50, 60]);

echo("Elements of Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nAdding elements in the deque\n");

// Use push() function to add elements
$deck->push(...[70, 80, 90, 100]);

echo("\nElements of Deque\n");

// Display the Deque elements
print_r($deck);

?>
```

**输出：**

```php
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

Adding elements in the deque

Elements of Deque
Ds\Deque Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
    [6] => 70
    [7] => 80
    [8] => 90
    [9] => 100
)

```

**引用：**[http://php.net/manual/en/ds-deque.push.php](http://php.net/manual/en/ds-deque.push.php)