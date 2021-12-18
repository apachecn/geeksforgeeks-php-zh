# PHP SplPriorityQueue Next()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-next-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-next-function/)

*SplPriorityQueue：：Next()*函数是 PHP 中的一个内置函数，用于从队列中提取顶级节点。

**语法：**

```php
void SplPriorityQueue::next()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

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

// Loop to print the priority
// queue elements
while($obj->valid()){

    // Print the current element
    echo $obj->current() . " ";

    // Move to next element of
    // priority queue
    $obj->next();
}

?>
```

**OUTPUT**

```php
G G4G Geeks GFG 
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.next.php](https://www.php.net/manual/en/splpriorityqueue.next.php)