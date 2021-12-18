# PHP|ds\Deque CONTAINS()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-contains-function-2/](https://www.geeksforgeeks.org/php-dsdeque-contains-function-2/)

**Ds\Deque：：CONTAINS()函数**是 PHP 中的一个内置函数，用于检查双端队列是否包含给定值。

**语法：**

```php
*bool* Ds\Deque::contains( $values )
```

**参数：**此函数接受单个或多个**$值**，这些值保存该值以检查该值是否存在于双队列中。

**返回值：**如果双队列中存在值，则返回 True，否则返回 False。

以下程序说明了 PHP 中的 DS\Deque：：CONTAINS()函数：

**程序 1：**

```php
<?php 

// Declare new Deque 
$deque = new \Ds\Deque(['G', 'e', 'e', 'k', 's', 5, 2, 7]); 

// Use contains() function to check elements 
// exist in the deque or not 
var_dump($deque->contains('G')); 

var_dump($deque->contains('k')); 

var_dump($deque->contains('p')); 

var_dump($deque->contains(7)); 

var_dump($deque->contains('5')); 

?> 
```

**输出：**

```php
bool(true)
bool(true)
bool(false)
bool(true)
bool(false)

```

**程序 2：**

```php
<?php 

// Declare new Deque 
$deque = new \Ds\Deque(['G', 'e', 'e', 'k', 's', 5, 2, 7]); 

// Use contains() function to check elements 
// exist in the deque or not 
var_dump($deque->contains('G', 'e')); 

var_dump($deque->contains('k', 'e', 7)); 

var_dump($deque->contains('p', '1')); 

var_dump($deque->contains(7, 1)); 

var_dump($deque->contains('5', 5)); 

?> 
```

**输出：**

```php
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/ds-deque.contains.php](https://www.php.net/manual/en/ds-deque.contains.php)