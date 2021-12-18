# PHP SplPriorityQueue Extract()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-extract-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-extract-function/)

SplPriorityQueue：：Extract()函数是 PHP 中的一个内置函数，用于从堆的顶部提取节点并向上筛选。

**语法：**

```
mixed SplPriorityQueue::extract()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数根据提取标志返回提取节点的值/优先级(或两者)。

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

// Display the extracted element
// from priority queue
var_dump($obj->extract());

?>
```

**OUTPUT**

```
string(1) "G"
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.extract.php](https://www.php.net/manual/en/splpriorityqueue.extract.php)