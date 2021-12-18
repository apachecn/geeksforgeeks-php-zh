# PHP|SplDoublyLinkedList POP()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-pop-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-pop-function/)

**SplDoublyLinkedList：：op()**函数是 PHP 中的一个内置函数，用于从双向链表的末尾弹出节点。

**语法：**

```
*mixed* SplDoublyLinkedList::pop( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回双向链表中弹出节点的值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：op()**函数：

**程序 1：**

```
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

// Use SplDoublyLinkedList::pop() function
// to remove elements from doubly linked list
var_dump($list->pop());
var_dump($list->pop());

?> 
```

**输出：**

```
string(1) "G"
string(5) "Geeks"

```

**程序 2：**

```
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

// Use SplDoublyLinkedList::pop() function
// to remove elements from doubly linked list
var_dump($list->pop());
var_dump($list->pop());
var_dump($list->pop());

?> 
```

**输出：**

```
int(5)
int(8)
int(3)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.pop.php](https://www.php.net/manual/en/spldoublylinkedlist.pop.php)