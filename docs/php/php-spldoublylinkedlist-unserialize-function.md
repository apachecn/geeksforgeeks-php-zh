# PHP|SplDoublyLinkedList unSerialize()函数

> Original: [https://www.geeksforgeeks.org/php-spldoublylinkedlist-unserialize-function/](https://www.geeksforgeeks.org/php-spldoublylinkedlist-unserialize-function/)

SplDoublyLinkedList：：UnSerialize()函数是 PHP 中的一个内置函数，用于反序列化 SplDoublyLinkedList：：Serialize()函数的存储。

**语法：**

```php
*void* SplDoublyLinkedList::unserialize( *string* $serialized )
```

**参数：**此函数接受保存序列化字符串的单个参数**$Serialized**。

**返回值：**此函数不返回任何值。

以下程序说明 PHP：
**程序 1：**中的 SplDoublyLinkedList：：UnSerialize()函数

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

// Use SplDoublyLinkedList::serialize() function
// to serialize the object
$serialize = serialize($list);

echo $serialize . "\n";

// Use SplDoublyLinkedList::unserialize() function
// to unserialize the object
$unserialze = unserialize($serialize);

print_r($unserialze);

?>
```

**Output:**

```php
C:19:"SplDoublyLinkedList":29:{i:0;:i:1;:i:2;:i:3;:i:8;:i:5;}
SplDoublyLinkedList Object
(
    [flags:SplDoublyLinkedList:private] => 0
    [dllist:SplDoublyLinkedList:private] => Array
        (
            [0] => 1
            [1] => 2
            [2] => 3
            [3] => 8
            [4] => 5
        )

)

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

// Use SplDoublyLinkedList::serialize() function
// to serialize the object
$serialize = serialize($list);

echo $serialize . "\n";

// Use SplDoublyLinkedList::unserialize() function
// to unserialize the object
$unserialze = unserialize($serialize);

print_r($unserialze);

?>
```

**Output:**

> C:19：”SplDoublyLinkedList”：105：{i:0；：s:7：”Welcome”；：s:2：”to”；：s:13：”GeeksforGeeks”；：s:1：”A”；：s:8：”Computer”；：s:7：”Science”；：s:6：”Portal”； }
> SplDoublyLinkedList 对象
> (
> [标志：SplDoublyLinkedList：Private]=>0
> [dllist：SplDoublyLinkedList：Private]=>Array
> (
> [0]=>Welcome
> [1]=>to
> [2]=>Geeksfort。 ][5]=>科学
> [6]=>门户
> )
> 
> )

**引用：**[https://www.php.net/manual/en/spldoublylinkedlist.unserialize.php](https://www.php.net/manual/en/spldoublylinkedlist.unserialize.php)