# PHP|SplDoublyLinkedList Shift()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-shift-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-shift-function/)

**SplDoublyLinkedList：：Shift()**函数是 PHP 中的一个内置函数，用于将节点从双向链表的开头移位。

**语法：**

```php
*mixed* SplDoublyLinkedList::shift( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回移位节点的值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：Shift()**函数：

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

// Use shift() function
var_dump($list->shift());
var_dump($list->shift());
var_dump($list->shift());

?> 
```

**输出：**

```php
int(30)
int(20)
int(30)

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

// Use shift() function
var_dump($list->shift());
var_dump($list->shift());
var_dump($list->shift());
var_dump($list->shift());

?> 
```

**输出：**

```php
int(1)
int(2)
int(3)
int(8)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.shift.php](https://www.php.net/manual/en/spldoublylinkedlist.shift.php)