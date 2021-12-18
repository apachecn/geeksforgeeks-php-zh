# PHP|Ds\Stack__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-dsstack-__construct-function/](https://www.geeksforgeeks.org/php-dsstack-__construct-function/)

**ds\Stack：：__Construct()函数**是 PHP 中的一个内置函数，用于创建一个新的堆栈实例。

**语法：**

```
*public* Ds\Stack::__construct( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要使用初始值的可遍历对象或数组。

下面的程序说明了 PHP 中的 Ds\Stack：：__Construct()函数：

**程序 1：**

```
<?php 

// Declare a new stack 
$stack = new \Ds\Stack(); 
print_r($stack); 

// Declare a new stack 
$stack = new \Ds\Stack(['G', 'E', 'K', 'S']); 
print_r($stack); 

?> 
```

**Output:**

```
Ds\Stack Object
(
)
Ds\Stack Object
(
    [0] => S
    [1] => K
    [2] => E
    [3] => G
)

```

**程序 2：**

```
<?php 

// Declare a new stack 
$stack = new \Ds\Stack([2, 3, 6, 7, 8]); 
var_dump($stack); 

// Declare a new stack 
$stack = new \Ds\Stack([2, 3, 5, 8, 9, 10]); 
var_dump($stack); 

?> 
```

**输出：**

```
object(Ds\Stack)#1 (5) {
  [0]=>
  int(8)
  [1]=>
  int(7)
  [2]=>
  int(6)
  [3]=>
  int(3)
  [4]=>
  int(2)
}
object(Ds\Stack)#2 (6) {
  [0]=>
  int(10)
  [1]=>
  int(9)
  [2]=>
  int(8)
  [3]=>
  int(5)
  [4]=>
  int(3)
  [5]=>
  int(2)
}

```

**引用：**[https://www.php.net/manual/en/ds-stack.construct.php](https://www.php.net/manual/en/ds-stack.construct.php)