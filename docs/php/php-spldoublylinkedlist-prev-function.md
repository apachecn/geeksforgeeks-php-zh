# PHP|SplDoublyLinkedList prev()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-prev-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-prev-function/)

**SplDoublyLinkedList：：prev()**函数是 PHP 中的一个内置函数，用于移动到上一个条目。

**语法：**

```php
*void* SplDoublyLinkedList::prev( void )
```

**参数：**此函数不接受任何参数。

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：prev()**函数：

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

// Use SplDoublyLinkedList::prev() function
// to move to previous entry
$list->prev();

// Display doubly linked list
print_r($list);

?> 
```

**输出：**

```php
SplDoublyLinkedList Object
(
    [flags:SplDoublyLinkedList:private] => 0
    [dllist:SplDoublyLinkedList:private] => Array
        (
            [0] => 30
            [1] => 20
            [2] => 30
            [3] => Geeks
            [4] => G
        )

)

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

// Use SplDoublyLinkedList::prev() function
// to move to previous entry
$list->prev();

// Display doubly linked list
var_dump($list);

?> 
```

**输出：**

```php
object(SplDoublyLinkedList)#1 (2) {
  ["flags":"SplDoublyLinkedList":private]=>
  int(0)
  ["dllist":"SplDoublyLinkedList":private]=>
  array(5) {
    [0]=>
    int(1)
    [1]=>
    int(2)
    [2]=>
    int(3)
    [3]=>
    int(8)
    [4]=>
    int(5)
  }
}

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.prev.php](https://www.php.net/manual/en/spldoublylinkedlist.prev.php)