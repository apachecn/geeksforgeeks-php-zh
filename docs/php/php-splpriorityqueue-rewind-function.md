# PHP SplPriorityQueue 倒带()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-rewind-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-rewind-function/)

SplPriorityQueue：：Rewind()函数是 PHP 中的一个内置函数，用于将迭代器倒回到起始位置。

**语法：**

```
voidSplPriorityQueue::rewind()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

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

// Use rewind() function
$obj->rewind();

// Print the priority queue elements
var_dump($obj->current());

?>
```

**OUTPUT**

```
string(1) "G"
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.rewind.php](https://www.php.net/manual/en/splpriorityqueue.rewind.php)