# PHP|SplQueue：：__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-splqueue__construct-function/](https://www.geeksforgeeks.org/php-splqueue__construct-function/)

**SplQueue：：__Construct()**函数是 PHP 中的一个内置函数，用于构造使用双向链表实现的队列。

**语法：**

```php
*void* SplQueue::__construct(void)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**SplQueue：：__Construct()**函数：

**程序 1：**

```php
<?php

// Create a new empty queue
$q = new SplQueue();

$q[] = 1;
$q[] = 2;
$q[] = 3;

// Print the queue elements
echo $q[0] . "\n";
echo $q[1] . "\n";
echo $q[2] . "\n";
?>
```

**输出：**

```php
1
2
3

```

**程序 2：**

```php
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
?>
```

**输出：**

```php
1
5
1
11
15
17

```

**引用：**[https://www.php.net/manual/en/splqueue.construct.php](https://www.php.net/manual/en/splqueue.construct.php)