# PHP|SplDoublyLinkedList Bottom()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-bottom-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-bottom-function/)

**SplDoublyLinkedList：：Bottom()**函数是 PHP 中的一个内置函数，用于从双向链表的开头查看节点值。

**语法：**

```php
*mixed* SplDoublyLinkedList::bottom( void )
```

**参数：**它不接受任何参数。

**返回值：**返回双向链表中第一个节点的值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：Bottom()**函数：

**程序 1：**

```php
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

// Use bottom() function
$val = $list->bottom();

// Display result
print_r($val); 

?> 
```

**输出：**

```php
1

```

**程序 2：**

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

// Use bottom() function
$val = $list->bottom();

// Display result
print_r($val); 

?> 
```

**输出：**

```php
30

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.bottom.php](https://www.php.net/manual/en/spldoublylinkedlist.bottom.php)