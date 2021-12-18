# PHP|SplDoublyLinkedList 推送()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-push-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-push-function/)

**SplDoublyLinkedList：：Push()**函数是 PHP 中的一个内置函数，用于推送双向链表末尾的元素。

**语法：**

```php
*void* SplDoublyLinkedList::push( $value )
```

**参数：**此函数接受单个参数**$value**，该参数保存一个元素以将其推送到双向链表的末尾。

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：Push()**函数：

**程序 1：**

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

// Display the elements of doubly linked list
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

**程序 2：**

```php
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList();

// Use SplDoublyLinkedList::push() function to 
// add elements to the SplDoublyLinkedList
$list->push("Welcome");
$list->push("to");
$list->push("GeeksforGeeks");
$list->push(5);

// Display the elements of doubly linked list
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
            [0] => Welcome
            [1] => to
            [2] => GeeksforGeeks
            [3] => 5
        )

)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.push.php](https://www.php.net/manual/en/spldoublylinkedlist.push.php)