# PHP SplPriorityQueue Insert()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-insert-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-insert-function/)

SplPriorityQueue：：Insert()函数是 PHP 中的一个内置函数，用于通过筛选元素在队列中插入元素。 按给定优先级在优先级队列中插入元素。

**语法：**

```php
bool SplPriorityQueue::insert( mixed $value, mixed $priority )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$value:** this parameter holds the value that needs to be inserted into the priority queue.
*   **$Priority:** this parameter saves the priority of the priority queue.

**返回值：**如果元素插入成功，此函数返回 TRUE。

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

// Display the priority queue elements
var_dump($obj);

?>
```

**OUTPUT**

```php
object(priorityQueue)#1 (3) {
  ["flags":"SplPriorityQueue":private]=>
  int(1)
  ["isCorrupted":"SplPriorityQueue":private]=>
  bool(false)
  ["heap":"SplPriorityQueue":private]=>
  array(4) {
    [0]=>
    array(2) {
      ["data"]=>
      string(1) "G"
      ["priority"]=>
      int(4)
    }
    [1]=>
    array(2) {
      ["data"]=>
      string(3) "G4G"
      ["priority"]=>
      int(3)
    }
    [2]=>
    array(2) {
      ["data"]=>
      string(5) "Geeks"
      ["priority"]=>
      int(2)
    }
    [3]=>
    array(2) {
      ["data"]=>
      string(3) "GFG"
      ["priority"]=>
      int(1)
    }
  }
}
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.insert.php](https://www.php.net/manual/en/splpriorityqueue.insert.php)