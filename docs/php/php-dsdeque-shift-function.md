# PHP|ds\Deque Shift()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-shift-function/](https://www.geeksforgeeks.org/php-dsdeque-shift-function/)

**ds\deeque：：Shift()**函数是 PHP 中的一个内置函数，用于删除和返回 deque 的第一个值。

**语法：**

```
*mixed* Ds\Deque::shift( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回删除的第一个 deque 值。

以下程序说明了 PHP 中的**ds\deque：：Shift()**函数：

**程序 1：**

```
<?php 

// Declare a deque 
$deq = new \Ds\Deque([10, 20, 30, 40, 50, 60]); 

// Use Ds\Deque::shift() function
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());

?> 
```

**输出：**

```
int(10)
int(20)
int(30)
int(40)
int(50)
int(60)

```

**程序 2：**

```
<?php 

// Declare a deque 
$deq = new \Ds\Deque(["geeks", "for", "geeks"]); 

// Use Ds\Deque::shift() function
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());

// Declare a deque 
$deq = new \Ds\Deque(['G', 'E', 'E', 'K', 'S', 1, 2, 3]); 

// Use Ds\Deque::shift() function
var_dump($deq -> shift());
var_dump($deq -> shift());
var_dump($deq -> shift());

?>
```

**输出：**

```
string(5) "geeks"
string(3) "for"
string(5) "geeks"
string(1) "G"
string(1) "E"
string(1) "E"

```

**引用：**[https://www.php.net/manual/en/ds-deque.shift.php](https://www.php.net/manual/en/ds-deque.shift.php)