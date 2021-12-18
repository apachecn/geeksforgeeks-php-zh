# PHP|SplDoublyLinkedList Serialize()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-serialize-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-serialize-function/)

**SplDoublyLinkedList：：Serialize()函数**是 PHP 中的内置函数，用于序列化存储。

**语法：**

```php
*string* SplDoublyLinkedList::serialize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回序列化字符串。

下面的程序演示了 PHP 中的 SplDoublyLinkedList：：Serialize()函数：

**程序 1：**

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

// Use serialize() function
$serialize = serialize($list);

echo $serialize;
?>
```

**输出：**

```php
C:19:"SplDoublyLinkedList":29:{i:0;:i:1;:i:2;:i:3;:i:8;:i:5;}

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

// Use serialize() function
$serialize = serialize($list);

echo $serialize;
?>
```

**输出：**

```php
C:19:"SplDoublyLinkedList":105:{i:0;:s:7:"Welcome";:s:2:
"to";:s:13:"GeeksforGeeks";:s:1:"A";:s:8:"Computer";
:s:7:"Science";:s:6:"Portal";}

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.serialize.php](https://www.php.net/manual/en/spldoublylinkedlist.serialize.php)