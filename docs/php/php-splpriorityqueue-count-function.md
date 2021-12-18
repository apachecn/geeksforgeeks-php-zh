# PHP SplPriorityQueue count()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-count-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-count-function/)

SplPriorityQueue：：count()函数是 PHP 中的一个内置函数，用于计算队列中的元素数量。

**语法：**

```
int SplPriorityQueue::count()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回队列中的元素数。

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

// Display the number of elements
// in priority queue
print_r($obj->count());

?>
```

**OUTPUT**

```
4
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.count.php](https://www.php.net/manual/en/splpriorityqueue.count.php)