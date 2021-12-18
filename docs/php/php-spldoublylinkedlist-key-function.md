# PHP|SplDoublyLinkedList key()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-key-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-key-function/)

**SplDoublyLinkedList：：key()**函数是 PHP 中的内置函数，用于返回当前节点的索引。

**语法：**

```
*mixed* SplDoublyLinkedList::key( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回当前节点的索引。

下面的程序演示了 PHP 中的 S**plDoublyLinkedList：：key()**函数：

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
$list->rewind();

// Use SplDoublyLinkedList::key() function
// to get the key
var_dump($list->key());

// Use next() function to increment
// the index value
$list->next();

// Use SplDoublyLinkedList::key() function
// to get the key
var_dump($list->key());

?> 
```

**输出：**

```
int(0)
int(1)

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

$list->rewind();

// Use SplDoublyLinkedList::key() function
// to get the key
var_dump($list->key());

// Use next() function to increment
// the index value
$list->next();
$list->next();
$list->next();

// Use SplDoublyLinkedList::key() function
// to get the key
var_dump($list->key());

?> 
```

**输出：**

```
int(0)
int(3)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.key.php](https://www.php.net/manual/en/spldoublylinkedlist.key.php)