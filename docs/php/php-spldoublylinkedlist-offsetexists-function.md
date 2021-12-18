# PHP|SplDoublyLinkedList offsetExists()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetexists-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetexists-function/)

**SplDoublyLinkedList：：offsetExists()**函数是 PHP 中的内置函数，用于检查给定索引是否存在。

**语法：**

```php
*bool* SplDoublyLinkedList::offsetExists( $index )
```

**参数：**此函数接受单个参数**$index**，该参数保存要检查的索引值。

**返回值：**如果给定索引存在，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：offsetExists()**函数：

**程序 1：**

```php
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList;

// Use SplDoublyLinkedList::add() function to 
// add elements to the SplDoublyLinkedList
$list->add(0, 30);
$list->add(1, 20);
$list->add(2, 30);
$list->add(3, "Geeks");
$list->add(4, 'G');
$list->rewind();

// Use SplDoublyLinkedList::offsetExists() function
// to check index exist or not
var_dump($list->offsetExists(2));

var_dump($list->offsetExists(10));

?> 
```

**输出：**

```php
bool(true)
bool(false)

```

**程序 2：**

```php
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList();

// Use SplDoublyLinkedList::push() function to 
// add elements to the SplDoublyLinkedList
$list->push(1);
$list->push(2);
$list->push(3);
$list->push(8);
$list->push(5);

// Use SplDoublyLinkedList::offsetExists() function
// to check index exist or not
var_dump($list->offsetExists(3));

var_dump($list->offsetExists(15));

?> 
```

**输出：**

```php
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.offsetexists.php](https://www.php.net/manual/en/spldoublylinkedlist.offsetexists.php)