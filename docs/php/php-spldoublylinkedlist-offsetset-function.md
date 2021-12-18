# PHP|SplDoublyLinkedList offsetSet()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetset-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetset-function/)

**SplDoublyLinkedList：：offsetSet()**函数是 PHP 中的内置函数，用于设置给定索引处的值。

**语法：**

```php
*void* SplDoublyLinkedList::offsetSet( $index, $newval )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$index:** it holds the index of the value to be set.
*   **$newval:** it holds the value to be set at the given index.

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：offsetSet()**函数：

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
$list->rewind();

// Use SplDoublyLinkedList::offsetSet() function
// to set the value at given index
$list->offsetSet(1, "GeeksforGeeks");

$list->offsetSet(2, "Welcome");

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
    int(30)
    [1]=>
    string(13) "GeeksforGeeks"
    [2]=>
    string(7) "Welcome"
    [3]=>
    string(5) "Geeks"
    [4]=>
    string(1) "G"
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
$list->push(1);
$list->push(2);
$list->push(3);
$list->push(8);
$list->push(5);

// Use SplDoublyLinkedList::offsetSet() function
// to set the value at given index
$list->offsetSet(1, "Welcome");

$list->offsetSet(2, "to");

$list->offsetSet(3, "GeeksforGeeks");

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
            [0] => 1
            [1] => Welcome
            [2] => to
            [3] => GeeksforGeeks
            [4] => 5
        )

)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.offsetset.php](https://www.php.net/manual/en/spldoublylinkedlist.offsetset.php)