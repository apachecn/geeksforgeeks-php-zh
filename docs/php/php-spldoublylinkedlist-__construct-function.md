# PHP|SplDoublyLinkedList__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-__construct-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-__construct-function/)

**SplDoublyLinkedList：：__Construction()函数**是 PHP 中的内置函数，用于创建新的空双向链表。

**语法：**

```
*public* SplDoublyLinkedList::__construct( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 SplDoublyLinkedList：：__Construct()函数：

**程序 1：**

```
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Push the element into SplDoublyLinkedList
$list->push(10);
$list->push(20);
$list->push(30);

// Display the SplDoublyLinkedList
var_dump($list);
?>
```

**输出：**

```
object(SplDoublyLinkedList)#1 (2) {
  ["flags":"SplDoublyLinkedList":private]=>
  int(0)
  ["dllist":"SplDoublyLinkedList":private]=>
  array(3) {
    [0]=>
    int(10)
    [1]=>
    int(20)
    [2]=>
    int(30)
  }
}

```

**程序 2：**

```
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Add the element into SplDoublyLinkedList
$list->add(0, "Welcome"); 
$list->add(1, "to"); 
$list->add(2, "GeeksforGeeks"); 
$list->add(3, "A"); 
$list->add(4, "Computer");
$list->add(5, "Science");
$list->add(6, "Portal");

// Display the SplDoublyLinkedList
var_dump($list);
?>
```

**输出：**

```
object(SplDoublyLinkedList)#1 (2) {
  ["flags":"SplDoublyLinkedList":private]=>
  int(0)
  ["dllist":"SplDoublyLinkedList":private]=>
  array(7) {
    [0]=>
    string(7) "Welcome"
    [1]=>
    string(2) "to"
    [2]=>
    string(13) "GeeksforGeeks"
    [3]=>
    string(1) "A"
    [4]=>
    string(8) "Computer"
    [5]=>
    string(7) "Science"
    [6]=>
    string(6) "Portal"
  }
}

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.construct.php](https://www.php.net/manual/en/spldoublylinkedlist.construct.php)