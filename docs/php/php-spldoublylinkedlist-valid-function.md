# PHP|SplDoublyLinkedList Valid()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-valid-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-valid-function/)

SplDoublyLinkedList：：Valid()函数是 PHP 中的一个内置函数，用于检查双向链表是否包含更多节点。

**语法：**

```php
*bool* SplDoublyLinkedList::valid( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果双向链表包含更多节点，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的 SplDoublyLinkedList：：Valid()函数

```php
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Use SplDoublyLinkedList::push() function to  
// add elements to the SplDoublyLinkedList 
$list->push(1); 
$list->push(2); 
$list->push(3); 
$list->push(8); 
$list->push(5); 

$list->rewind();

for($i = 0; $i < 5; $i++) {
    if($list->valid())
        echo $list->current() . " ";

    $list->next();
}

?>
```

**Output:**

```php
1 2 3 8 5

```

**程序 2：**

```php
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Use SplDoublyLinkedList::add() function
// to add the element into the list
$list->add(0, "Welcome"); 
$list->add(1, "to"); 
$list->add(2, "GeeksforGeeks"); 
$list->add(3, "A"); 
$list->add(4, 'Computer'); 
$list->add(5, "Science"); 
$list->add(6, 'Portal'); 

$list->rewind();

for($i = 0; $i < 7; $i++) {
    if($list->valid())
        echo $list->current() . " ";

    $list->next();
}

?>
```

**Output:**

```php
Welcome to GeeksforGeeks A Computer Science Portal

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.valid.php](https://www.php.net/manual/en/spldoublylinkedlist.valid.php)