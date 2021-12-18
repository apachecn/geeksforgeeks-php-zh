# PHP|SplQueue：：EnQueue()函数

> Original: [https://www.geeksforgeeks.org/php-splqueueenqueue-function/](https://www.geeksforgeeks.org/php-splqueueenqueue-function/)

**SplQueue：：enQueue()**函数是 PHP 中的一个内置函数，用于将元素添加到队列中。

**语法：**

```
*void* SplQueue::enqueue( $val )
```

**参数：**此函数接受单个参数**$val**，该参数指定 add(入队)元素的值。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**SplQueue：：enQueue()**函数：

**程序 1：**

```
<?php

// Create a new empty queue
$gfg = new SplQueue();

$gfg[] = 1;

// Enqueue element
$gfg->enqueue(10);
$gfg->enqueue(20);

echo $gfg[1] .  "\n";
echo $gfg[2] .  "\n";

?>
```

**输出：**

```
10
20

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

$gfg->enqueue(11);
$gfg->enqueue(12);
$gfg->enqueue(13);
$gfg->enqueue(14);

// Print result after enqueue
foreach ($gfg as $elem)  {
    echo $elem."\n";
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
11
12
13
14

```

**引用：**[https://www.php.net/manual/en/splqueue.enqueue.php](https://www.php.net/manual/en/splqueue.enqueue.php)