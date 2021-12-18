# PHP|SplHeap count()函数

> Original: [https://www.geeksforgeeks.org/php-splheap-count-function/](https://www.geeksforgeeks.org/php-splheap-count-function/)

SplHeap：：Count()函数是 PHP 中的一个内置函数，用于对堆中的元素进行计数。
通常，[堆](https://www.geeksforgeeks.org/heap-data-structure/)可以是两种类型：

*   **Max-Heap：**在 Max-Heap 中，根节点上出现的键必须是其所有子节点上出现的键中最大的。 对于该二叉树中的所有子树，相同的属性必须递归为真。
*   **Min-Heap：**在 Min-Heap 中，根节点上出现的键必须是其所有子节点上出现的键中的最小键。 对于该二叉树中的所有子树，相同的属性必须递归为真。

**注意：**本文使用扩展 SplHeap 类的 Max Heap。

**语法：**

```php
*int* SplMaxHeap::count()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回堆中存在的节点数。

下面的程序演示了 PHP 中的 SplMaxHeap：：Count()函数：

**程序 1：**

```php
<?php

// Create a new empty Max Heap
$heap = new SplMaxHeap();

$heap->insert('GEEKS');
$heap->insert('gfg');

// Print Result
echo $heap->count();

?>
```

**Output:**

```php
2

```

**程序 2：**

```php
<?php

// Create a new empty Max Heap
$heap = new SplMaxHeap();

// Print Result
echo $heap->count() . "\n";

$heap->insert('GEEKS');
$heap->insert('gfg');
$heap->insert('DSA');
$heap->insert('ALGO');
$heap->insert('C');

// Print Result
echo $heap->count();

?>
```

**Output:**

```php
0
5

```

**引用：**[https://www.php.net/manual/en/splheap.count.php](https://www.php.net/manual/en/splheap.count.php)