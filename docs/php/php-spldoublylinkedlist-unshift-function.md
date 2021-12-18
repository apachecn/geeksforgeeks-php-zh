# PHP|SplDoublyLinkedList unShift()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-unshift-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-unshift-function/)

**SplDoublyLinkedList：：unShift()**函数是 PHP 中的一个内置函数，用于将元素添加到双向链表的开头。

**语法：**

```php
*void* SplDoublyLinkedList::unshift( $value )
```

**参数：**此函数接受单个参数**$value**，该参数用于取消双向链表中的值的移位。

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：UnShift()**函数：

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

// Use unshift() function
$list->unshift("GeeksforGeeks");

// Display the list elements
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
            [0] => GeeksforGeeks
            [1] => 30
            [2] => 20
            [3] => 30
            [4] => Geeks
            [5] => G
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

// Use unshift() function
$list->unshift("Geeks");

// Display the list elements
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
            [0] => Geeks
            [1] => 1
            [2] => 2
            [3] => 3
            [4] => 8
            [5] => 5
        )

)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.unshift.php](https://www.php.net/manual/en/spldoublylinkedlist.unshift.php)