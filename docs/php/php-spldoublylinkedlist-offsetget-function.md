# PHP|SplDoublyLinkedList offsetGet()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetget-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetget-function/)

**SplDoublyLinkedList：：offsetGet()**函数是 PHP 中的一个内置函数，它返回给定索引处的值。

**语法：**

```php
*mixed* SplDoublyLinkedList::offsetGet( $index )
```

**参数：**此函数接受保存索引值的单个参数**$index**。

**返回值：**它返回给定索引处的值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：offsetGet()**函数：

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

// Use SplDoublyLinkedList::offsetGet() function
// to check index exist or not
var_dump($list->offsetGet(2));

var_dump($list->offsetGet(3));

?> 
```

**输出：**

```php
int(30)
string(5) "Geeks"

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

// Use SplDoublyLinkedList::offsetGet() function
// to check index exist or not
var_dump($list->offsetGet(1));
var_dump($list->offsetGet(2));
var_dump($list->offsetGet(3));

?> 
```

**输出：**

```php
int(2)
int(3)
int(8)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.offsetget.php](https://www.php.net/manual/en/spldoublylinkedlist.offsetget.php)