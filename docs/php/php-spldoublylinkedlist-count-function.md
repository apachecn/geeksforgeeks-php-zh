# PHP|SplDoublyLinkedList count()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-count-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-count-function/)

**SplDoublyLinkedList：：count()**函数是 PHP 中的一个内置函数，用于计算双向链表中存在的元素数量。

**语法：**

```
*int* SplDoublyLinkedList::count( void )
```

**参数：**不包含任何参数。

**返回值：**返回双向链表中存在的元素个数。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：Count()**函数：

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

// Use SplDoublyLinkedList::count() function
// to return number of elements
print_r($list->count());

?> 
```

**输出：**

```
5

```

**程序 2：**

```
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList;

// Use SplDoublyLinkedList::push() function to 
// add elements to the SplDoublyLinkedList
$list->push(1);
$list->push(2);
$list->push(3);
$list->push(8);
$list->push(5);

// Use SplDoublyLinkedList::count() function
// to return number of elements
print_r($list->count());

?> 
```

**输出：**

```
5

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.count.php](https://www.php.net/manual/en/spldoublylinkedlist.count.php)