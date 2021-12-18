# PHP|SplDoublyLinkedList setIteratorMode()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-setiteratormode-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-setiteratormode-function/)

SplDoublyLinkedList：：setIteratorMode()函数是 PHP 中的内置函数，用于设置迭代模式。

**语法：**

```
*void* SplDoublyLinkedList::setIteratorMode( *int* $mode )
```

**参数：**此函数接受单个参数**$mode**，该参数包含下面列出的两组正交模式：
迭代方向为：

*   SplDoublyLinkedList：：IT_MODE_LIFO(堆栈样式)
*   SplDoublyLinkedList：：IT_MODE_FIFO(队列样式)

迭代器的行为包括：

*   SplDoublyLinkedList：：it_mode_delete(元素由迭代器删除)
*   SplDoublyLinkedList：：IT_MODE_KEEP(迭代器遍历元素)

**返回值：**此函数不返回任何值。

以下程序说明 PHP：
**程序 1：**中的 SplDoublyLinkedList：：setIteratorMode()函数

```
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Add the element into SplDoublyLinkedList
$list->setIteratorMode(SplDoublyLinkedList::IT_MODE_FIFO); 

// Use getIteratorMode() function
$mode = $list->getIteratorMode();
var_dump($mode);

// Add the element into SplDoublyLinkedList
$list->setIteratorMode(SplDoublyLinkedList::IT_MODE_DELETE); 

// Use getIteratorMode() function
$mode = $list->getIteratorMode();
var_dump($mode);

// Add the element into SplDoublyLinkedList
$list->setIteratorMode(SplDoublyLinkedList::IT_MODE_LIFO); 

// Use getIteratorMode() function
$mode = $list->getIteratorMode();
var_dump($mode);

?>
```

**Output:**

```
int(0)
int(1)
int(2)

```

**程序 2：**

```
<?php

// Declare an empty SplDoublyLinkedList 
$list = new SplDoublyLinkedList();

// Add the element into SplDoublyLinkedList
$list->setIteratorMode(SplDoublyLinkedList::IT_MODE_FIFO
                    | SplDoublyLinkedList::IT_MODE_DELETE
                    | SplDoublyLinkedList::IT_MODE_LIFO); 

$mode = $list->getIteratorMode();

var_dump($mode & SplDoublyLinkedList::IT_MODE_FIFO);

var_dump($mode & SplDoublyLinkedList::IT_MODE_LIFO);

var_dump($mode & SplDoublyLinkedList::IT_MODE_DELETE);

var_dump($mode & SplDoublyLinkedList::IT_MODE_KEEP); 

?>
```

**Output:**

```
int(0)
int(2)
int(1)
int(0)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.setiteratormode.php](https://www.php.net/manual/en/spldoublylinkedlist.setiteratormode.php)