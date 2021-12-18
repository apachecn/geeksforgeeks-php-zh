# PHP|SplDoublyLinkedList getIteratorMode()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-getiteratormode-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-getiteratormode-function/)

**SplDoublyLinkedList：：getIteratorMode()函数**是 PHP 中的内置函数，用于返回迭代模式。

**语法：**

```
*int* SplDoublyLinkedList::getIteratorMode( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回影响迭代的不同模式和标志。

下面的程序演示了 PHP 中的 SplDoublyLinkedList：：getIteratorMode()函数：

**程序 1：**

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

**输出：**

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

**输出：**

```
int(0)
int(2)
int(1)
int(0)

```

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.getiteratormode.php](https://www.php.net/manual/en/spldoublylinkedlist.getiteratormode.php)