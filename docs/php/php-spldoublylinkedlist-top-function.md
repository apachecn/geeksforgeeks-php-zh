# PHP|SplDoublyLinkedList top()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-top-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-top-function/)

**SplDoublyLinkedList：：top()**函数是 PHP 中的一个内置函数，用于返回双向链表中最后一个(Top)节点的值。

**语法：**

```php
*mixed* SplDoublyLinkedList::top( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回双向链表中最后一个节点的值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：top()**函数：

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

// Use top() function
var_dump($list->top());

?> 
```

**输出：**

```php
string(1) "G"

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

// Use top() function
var_dump($list->top());

?> 
```

**输出：**

```php
int(5)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.top.php](https://www.php.net/manual/en/spldoublylinkedlist.top.php)