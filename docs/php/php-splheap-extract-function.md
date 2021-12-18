# PHP SplHeap Extract()函数

> Original: [https://www.geeksforgeeks.org/php-splheap-extract-function/](https://www.geeksforgeeks.org/php-splheap-extract-function/)

SplHeap：：Extract()函数是 PHP 中的一个内置函数，用于从堆的顶部提取节点并向上筛选。

通常，堆数据结构有两种类型：

*   **max-heap:** in Max-Heap, the key that appears on the root node must be the largest of all the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.
*   **Min-Heap:** in Min-Heap, the key that appears on the root node must be the smallest of the keys that appear on all its child nodes. For all subtrees in the binary tree, the same attribute must be recursive to true.

**语法：**

```
mixed SplHeap::extract()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回提取的节点的值。

下面的程序演示了 PHP 中的 SplHeap：：Extract()函数：

**示例 1：**

## PHP

```
<?php 

// Create a new empty Min Heap 
$heap = new SplMinHeap(); 

$heap->insert('System'); 
$heap->insert('GFG'); 
$heap->insert('ALGO'); 
$heap->insert('C');
$heap->insert('Geeks'); 
$heap->insert('GeeksforGeeks'); 

echo $heap->extract();

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

## PHP

```
<?php 

// Create a new empty Max Heap 
$heap = new SplMaxHeap(); 

$heap->insert('System'); 
$heap->insert('GFG'); 
$heap->insert('ALGO'); 
$heap->insert('C');
$heap->insert('Geeks'); 
$heap->insert('GeeksforGeeks'); 

echo $heap->extract();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/splheap.extract.php](https://www.php.net/manual/en/splheap.extract.php)