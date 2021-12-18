# PHP|SplDoublyLinkedList add()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-add-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-add-function/)

**SplDoublyLinkedList：：add()**函数是 PHP 中的内置函数，用于在给定索引处添加新值。

**语法：**

```
*void* SplDoublyLinkedList::add( $index, $newval )
```

**参数：**如上所述，它包含两个参数：

*   **$index:** it holds the index value of the new element to be inserted.
*   **$newval:** it holds the elements to be inserted or added.

**返回值：**不返回任何值。

下面的程序演示了 PHP 中的**SplDoublyLinkedList：：add()**函数：

**程序 1：**

```
<?php 

// Declare an empty SplDoublyLinkedList
$list = new \SplDoublyLinkedList;

// Use SplDoublyLinkedList::add() function to 
// add elements to the SplDoublyLinkedList
$list->add(0, 1); 

$list->add(1, "Geeks"); 

$list->add(2, "G"); 

$list->add(3, 10); 

print_r($list); 
?> 
```

**输出：**

```
SplDoublyLinkedList Object
(
    [flags:SplDoublyLinkedList:private] => 0
    [dllist:SplDoublyLinkedList:private] => Array
        (
            [0] => 1
            [1] => Geeks
            [2] => G
            [3] => 10
        )

)

```

**程序 2：**

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

print_r($list); 
?> 
```

**输出：**

```
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

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.add.php](https://www.php.net/manual/en/spldoublylinkedlist.add.php)