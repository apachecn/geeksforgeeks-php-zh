# PHP|SplHeap Current()函数

> Original: [https://www.geeksforgeeks.org/php-splheap-current-function/](https://www.geeksforgeeks.org/php-splheap-current-function/)

SplHeap：：Current()函数是 PHP 中的一个内置函数，用于获取迭代器指向的当前元素。

通常，[堆数据结构](https://www.geeksforgeeks.org/heap-data-structure/)有两种类型：

*   **Max-Heap:** in Max-Heap, the key that appears on the root node must be the largest of all the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.
*   **Min-Heap:** in Min-Heap, the key that appears on the root node must be the smallest of the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.

**注意：**本文使用扩展 SplHeap 类的 Max Heap。

**语法：**

```php
*mixed* SplMaxHeap::current()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回堆数据结构的当前节点。

下面的程序演示了 PHP 中的 SplMaxHeap：：Current()函数：

**程序 1：**

```php
<?php

// Create a new empty Max Heap
$heap = new SplMaxHeap();

$heap->insert('System');
$heap->insert('gfg');
$heap->insert('ALGO');
$heap->insert('C');

// Move next node
$heap->next();
$heap->next();

echo $heap->current() . "\n";
?>
```

**输出：**

```php
C

```

**程序 2：**

```php
<?php

// Create a new empty Max Heap
$heap = new SplMaxHeap();

$heap->insert('GEEKS');
$heap->insert('gfg');
$heap->insert('DSA');
$heap->insert('ALGO');
$heap->insert('C');

// Iterate array and print values
while($heap->valid()) {

    // Print current value of index of the array
    echo $heap->current(). "\n";

    // Move next each time of iteration
    $heap->next();
}

?>
```

**输出：**

```php
gfg
GEEKS
DSA
C
ALGO

```

**引用：**[https://www.php.net/manual/en/splheap.current.php](https://www.php.net/manual/en/splheap.current.php)