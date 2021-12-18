# PHP|SplDoublyLinkedList isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-isempty-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-isempty-function/)

**SplDoublyLinkedList：：isEmpty()**函数是 PHP 中的内置函数，用于检查双向链表是否为空。

**语法：**

```
*bool* SplDoublyLinkedList::isEmpty( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果双向链表为空，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：isEmpty()**函数：

**程序 1：**

```
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList;

// Use isEmpty function 
$res = $list->isEmpty(); 

var_dump($res);

// Use SplDoublyLinkedList::push() function to 
// add elements to the SplDoublyLinkedList
$list->push(1);
$list->push(2);
$list->push(3);
$list->push(8);
$list->push(5);

// Use isEmpty function 
$res = $list->isEmpty(); 

var_dump($res);

?> 
```

**输出：**

```
bool(true)
bool(false)

```

**程序 2：**

```
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList;

// Use isEmpty function 
$res = $list->isEmpty(); 

var_dump($res);

// Use SplDoublyLinkedList::add() function to 
// add elements to the SplDoublyLinkedList
$list->add(0, 30);
$list->add(1, 20);
$list->add(2, 30);
$list->add(3, "Geeks");
$list->add(4, 'G');

// Use isEmpty function 
$res = $list->isEmpty(); 

var_dump($res);

?> 
```

**输出：**

```
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.isempty.php](https://www.php.net/manual/en/spldoublylinkedlist.isempty.php)