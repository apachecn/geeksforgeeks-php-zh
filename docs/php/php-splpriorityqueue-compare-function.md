# PHP SplPriorityQueue Compare()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-compare-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-compare-function/)

SplPriorityQueue：：Compare()函数是 PHP 中的一个内置函数，用于比较要在堆数据结构中按特定顺序放置的优先级队列元素。

**语法：**

```
int SplPriorityQueue::compare( 
    mixed $priority1 , mixed $priority2 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **priority1:** this parameter holds the priority of the first node being compared.
*   **priority 2:** this parameter saves the priority of the second node being compared.

**返回值：**此函数返回比较函数的结果。 如果优先级 1 大于优先级 2，则返回+ve 整数，如果两者相等，则返回 0，否则返回-ve 整数。

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

// Display the priority queue elements
var_dump($obj);

?>
```

**OUTPUT**

```
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

**引用：**[https://www.php.net/manual/en/splpriorityqueue.compare.php](https://www.php.net/manual/en/splpriorityqueue.compare.php)