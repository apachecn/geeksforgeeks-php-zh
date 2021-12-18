# PHP|SplDoublyLinkedList offsetUnset()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetunset-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-offsetunset-function/)

**SplDoublyLinkedList：：offsetUnset()**函数是 PHP 中的一个内置函数，用于取消设置给定索引处的值。

**语法：**

```php
*void* SplDoublyLinkedList::offsetUnset( $index )
```

**参数：**此函数接受单个参数**$index**，该参数保存要取消设置其值的索引值。

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：offsetUnset()**函数：

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

// Use SplDoublyLinkedList::offsetUnset() function
// to unset the value at given index
$list->offsetUnset(0);

$list->offsetUnset(1);

$list->offsetUnset(0);

$list->offsetUnset(1);

var_dump($list);

?> 
```

**输出：**

```php
object(SplDoublyLinkedList)#1 (2) {
  ["flags":"SplDoublyLinkedList":private]=>
  int(0)
  ["dllist":"SplDoublyLinkedList":private]=>
  array(1) {
    [0]=>
    string(5) "Geeks"
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

// Use SplDoublyLinkedList::offsetUnset() function
// to unset the value at given index
$list->offsetUnset(1);

$list->offsetUnset(2);

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
            [1] => 3
            [2] => 5
        )

)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.offsetunset.php](https://www.php.net/manual/en/spldoublylinkedlist.offsetunset.php)