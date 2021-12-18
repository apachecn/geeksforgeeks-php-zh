# PHP SplPriorityQueue key()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-key-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-key-function/)

*SplPriorityQueue：：key()*函数是 PHP 中的内置函数，用于返回当前节点索引。

**语法：**

```
mixed SplPriorityQueue::key()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前节点索引。

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

// Use key() function to get the 
// current key of priority queue
var_dump($obj->key());

?>
```

**OUTPUT**

```
int(3)
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.key.php](https://www.php.net/manual/en/splpriorityqueue.key.php)