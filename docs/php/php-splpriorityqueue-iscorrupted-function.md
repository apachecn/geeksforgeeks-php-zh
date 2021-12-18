# PHP SplPriorityQueue isCorrupted()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-iscorrupted-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-iscorrupted-function/)

*SplPriorityQueue：：isCorrupted()*函数是 PHP 中的一个内置函数，用于告知优先级队列是否处于损坏状态。

**语法：**

```
bool SplPriorityQueue::isCorrupted()
```

**参数：**此函数不接受任何参数。

**返回值：**如果优先级队列处于损坏状态，则此函数返回 TRUE，否则返回 FALSE。

**示例：**

## PHP

```
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

// Use isCorrupted() function to check
// priority queue is in corrupted state
// or not
var_dump($obj->isCorrupted());

?>
```

**OUTPUT**

```
bool(false)
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.iscorrupted.php](https://www.php.net/manual/en/splpriorityqueue.iscorrupted.php)