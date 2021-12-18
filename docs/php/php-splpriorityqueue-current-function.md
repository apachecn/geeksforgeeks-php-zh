# PHP SplPriorityQueue Current()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-current-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-current-function/)

SplPriorityQueue：：Current()函数是 PHP 中的一个内置函数，用于返回迭代器指向的当前节点。

**语法：**

```php
mixed SplPriorityQueue::current()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数根据提取标志返回当前节点的值/优先级。

**示例：**

## PHP

```php
<?php

// Declare a class
class priorityQueue extends SplPriorityQueue {

    // Compare function to compare priority
    // queue elements
    public function compare($p1, $p2) {
        if ($p1 === $p2) return 0;
        return $p1 < $p2 ? -1 : 1;
    }
}

// Create an object of priority queue
$obj = new priorityQueue();

// Insert elements into the queue
$obj->insert("Geeks",2);
$obj->insert("GFG",1);
$obj->insert("G4G",3);
$obj->insert('G',4);

// Display the current element
// of priority queue
print_r($obj->current());

?>
```

**OUTPUT**

```php
G
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.current.php](https://www.php.net/manual/en/splpriorityqueue.current.php)