# PHP|SplDoublyLinkedList Next()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-next-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-next-function/)

**SplDoublyLinkedList：：Next()**函数是 PHP 中的一个内置函数，用于将索引移到下一个索引中。

**语法：**

```
*void* SplDoublyLinkedList::next( void )
```

**参数：**此函数不接受任何参数。

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：Next()**函数：

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

// Use SplDoublyLinkedList::current() function
// to get the current element
var_dump($list->current());

// Use next() function to increment
// the index value
$list->next();

// Use SplDoublyLinkedList::current() function
// to get the current element
var_dump($list->current());

?> 
```

**输出：**

```
int(30)
int(20)

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

// Use SplDoublyLinkedList::current() function
// to get the current element
var_dump($list->current());

// Use next() function to increment
// the index value
$list->next();
$list->next();
$list->next();

// Use SplDoublyLinkedList::current() function
// to get the current element
var_dump($list->current());

?> 
```

**输出：**

```
int(1)
int(8)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.next.php](https://www.php.net/manual/en/spldoublylinkedlist.next.php)