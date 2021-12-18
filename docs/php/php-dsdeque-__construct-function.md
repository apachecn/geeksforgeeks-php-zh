# PHP|ds\deeque__struct()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-__construct-function/](https://www.geeksforgeeks.org/php-dsdeque-__construct-function/)

**ds\deeque：：__struct()**函数是 PHP 中的内置函数，用于创建新实例。

**语法：**

```
Ds\Deque::__construct( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要使用初始值的可遍历对象或数组。

以下程序说明了 PHP 中的**ds\deque：：__struct()**函数：

**程序 1：**

```
<?php 

// Declare a deque 
$deq = new \Ds\Deque();

// Display the elements of deque
echo("Elements of first deque:\n"); 
var_dump($deq);

// Declare a deque 
$deq = new \Ds\Deque([10, 20, 30, 40, 50, 60]); 

// Display the elements of deque
echo("\nElements of second deque:\n"); 
var_dump($deq);

?>
```

**Output:**

```
Elements of first deque:
object(Ds\Deque)#1 (0) {
}

Elements of second deque:
object(Ds\Deque)#2 (6) {
  [0]=>
  int(10)
  [1]=>
  int(20)
  [2]=>
  int(30)
  [3]=>
  int(40)
  [4]=>
  int(50)
  [5]=>
  int(60)
}

```

**程序 2：**

```
<?php 

// Declare a deque 
$deq = new \Ds\Deque(["geeks", "for", "geeks"]); 

// Display the elements of deque
echo("Elements of first deque:\n"); 
print_r($deq);

// Declare a deque 
$deq = new \Ds\Deque(['G', 'E', 'E', 'K', 'S', 1, 2, 3]); 

// Display the elements of deque
echo("\nElements of second deque:\n"); 
print_r($deq);

?>
```

**输出：**

```
Elements of first deque:
Ds\Deque Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)

Elements of second deque:
Ds\Deque Object
(
    [0] => G
    [1] => E
    [2] => E
    [3] => K
    [4] => S
    [5] => 1
    [6] => 2
    [7] => 3
)

```

**引用：**[https://www.php.net/manual/en/ds-deque.construct.php](https://www.php.net/manual/en/ds-deque.construct.php)