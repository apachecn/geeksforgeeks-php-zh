# PHP|SplQueue：：DeQueue()函数

> Original: [https://www.geeksforgeeks.org/php-splqueuedequeue-function/](https://www.geeksforgeeks.org/php-splqueuedequeue-function/)

**SplQueue：：DeQueue()**函数是 PHP 中的一个内置函数，用于将节点从队列中出列。

**语法：**

```
*mixed* SplQueue::dequeue()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回出列节点的值。

下面的程序演示了 PHP 中的**SplQueue：：DeQueue()**函数：

**程序 1：**

```
<?php

// Create a new empty queue
$gfg = new SplQueue();

$gfg[] = 1;
$gfg[] = 2;
$gfg[] = 3;

// Dequeue element
echo $gfg->dequeue() . "\n";
echo $gfg->dequeue() . "\n";

?>
```

**输出：**

```
1
2

```

**程序 2：**

```
<?php

// Create some fixed size array
$gfg = new SplQueue();

$gfg[] = 1;
$gfg[] = 5;
$gfg[] = 1;
$gfg[] = 11;
$gfg[] = 15;
$gfg[] = 17;

foreach ($gfg as $elem)  {
    echo $elem . "\n";
}

$gfg->dequeue();
$gfg->dequeue();
$gfg->dequeue();

// Print result after dequeue
foreach ($gfg as $elem)  {
    echo "dequeue: " . $gfg->dequeue() . "\n";

}
?>
```

**输出：**

```
1
5
1
11
15
17
dequeue: 11
dequeue: 15
dequeue: 17

```

**引用：**[https://www.php.net/manual/en/splqueue.dequeue.php](https://www.php.net/manual/en/splqueue.dequeue.php)