# PHP|ds\Deque find()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-find-function/](https://www.geeksforgeeks.org/php-dsdeque-find-function/)

**Ds\Deque：：find()**函数是 PHP 中的一个内置函数，用于查找在 Deque 中找到的 Deque if 元素中的元素的索引。
**语法：**和

```php
*public* Ds\Deque::find( $value ) : mixed
```

**参数：**此函数接受单个参数*$value*，该参数保存要找到其索引的元素。
**返回值：**如果元素存在，则此函数返回元素的索引，否则返回 FALSE。
下面的程序说明了 PHP：
**程序 1：**和
中的**Ds\Deque：：Find()**函数

## PHP

```php
<?php

// Declare a deque
$deck = new \Ds\Deque([10, 20, 3, 40, 50, 6]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nIndex of 3 in the deque: ");

// Use find() function to find
// the index of element
print_r($deck->find(3));

?>
```

发帖主题：Re：Колибри0.7.0

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
Index of 3 in the deque: 2
```

**程序 2：**

## PHP

```php
<?php

// Declare a deque
$deck = new \Ds\Deque(["Geeks", "for", "GFG"]);

echo("Elements in the Deque\n");

// Display the Deque elements
print_r($deck);

echo("\nIndex of 3 in the deque: ");

// Use find() function to find
// the index of element
var_dump($deck->find("ABC"));

?>
```

发帖主题：Re：Колибри0.7.0

```php
Elements in the Deque
Ds\Deque Object
(
   [0] => Geeks
   [1] => for
   [2] => GFG
)
Index of 3 in the deque: bool(false)
```

**引用：**[http://php.net/manual/en/ds-deque.find.php](http://php.net/manual/en/ds-deque.find.php)