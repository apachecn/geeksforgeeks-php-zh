# PHP SplHeap isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-splheap-isempty-function/](https://www.geeksforgeeks.org/php-splheap-isempty-function/)

SplHeap：：isEmpty()函数是 PHP 中的一个内置函数，用于检查堆是否为空。

通常，堆数据结构有两种类型：

*   **max-heap:** in Max-Heap, the key that appears on the root node must be the largest of all the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.
*   **Min-Heap:** in Min-Heap, the key that appears on the root node must be the smallest of the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.

**语法：**

```
bool SplHeap::isEmpty()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回堆是否为空。

下面的程序演示了 PHP 中的 SplHeap：：isEmpty()函数：

**示例 1：**

## PHP

```
<?php 

// Create a new empty Max Heap 
$heap1 = new SplMaxHeap(); 

// Create a new empty Max Heap 
$heap2 = new SplMaxHeap(); 

// Insert elements in max heap
$heap2->insert('System'); 
$heap2->insert('GFG'); 

// Check heap is empty or not
var_dump($heap1->isEmpty());

var_dump($heap2->isEmpty());

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

## PHP

```
<?php 

// Create a new empty Min Heap 
$heap1 = new SplMinHeap(); 

// Create a new empty Max Heap 
$heap2 = new SplMinHeap(); 

// Insert elements in min heap
$heap2->insert('System'); 
$heap2->insert('GFG'); 

// Check heap is empty or not
var_dump($heap1->isEmpty());

var_dump($heap2->isEmpty());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/splheap.isempty.php](https://www.php.net/manual/en/splheap.isempty.php)