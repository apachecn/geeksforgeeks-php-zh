# PHP SplPriorityQueue isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-splpriorityqueue-isempty-function/](https://www.geeksforgeeks.org/php-splpriorityqueue-isempty-function/)

*SplPriorityQueue：：isEmpty()*函数是 PHP 中的内置函数，用于检查队列是否为空。

**语法：**

```php
bool SplPriorityQueue::isEmpty()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回布尔值*true*或*false*，具体取决于队列是否为空。

**示例 1：**

## PHP

```php
<?php

// Declare empty class
class priorityQueue extends SplPriorityQueue {
}

// Create an object of priority queue
$obj = new priorityQueue();

// Use isEmpty() function to check
// priority queue is empty or not
var_dump($obj->isEmpty());

?>
```

**OUTPUT**

```php
bool(true)
```

**示例 2：**

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

// Use isEmpty() function to check
// priority queue is empty or not
var_dump($obj->isEmpty());

?>
```

**OUTPUT**

```php
bool(false)
```

**引用：**[https://www.php.net/manual/en/splpriorityqueue.isempty.php](https://www.php.net/manual/en/splpriorityqueue.isempty.php)