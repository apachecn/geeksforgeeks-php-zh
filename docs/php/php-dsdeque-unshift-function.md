# PHP|ds\Deque unShift()函数

> Original: [https://www.geeksforgeeks.org/php-dsdeque-unshift-function/](https://www.geeksforgeeks.org/php-dsdeque-unshift-function/)

**Ds\Deque：：unShift()**函数是 PHP 中的一个内置函数，用于将值添加到 deque 前面。

**语法：**

```php
*void* Ds\Deque::unshift( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要以双队列字体添加的值。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**Ds\Deque：：UnShift()**函数：

**程序 1：**

```php
<?php 

// Declare a deque 
$deq = new \Ds\Deque([10, 20, 30, 40]); 

// Use Ds\Deque::unshift() function
$deq -> unshift(5);
$deq -> unshift(7);
$deq -> unshift(8);

print_r($deq);

?> 
```

**输出：**

```php
Ds\Deque Object
(
    [0] => 8
    [1] => 7
    [2] => 5
    [3] => 10
    [4] => 20
    [5] => 30
    [6] => 40
)

```

**程序 2：**

```php
<?php 

// Declare a deque 
$deq = new \Ds\Deque(); 

// Use Ds\Deque::unshift() function
$deq -> unshift("Welcome");
$deq -> unshift("to");
$deq -> unshift("GeeksforGeeks");

var_dump($deq);

// Declare another deque 
$deq = new \Ds\Deque(['G', 'E', 'E', 'K', 'S']); 

// Use Ds\Deque::unshift() function
$deq -> unshift("1");
$deq -> unshift("2");
$deq -> unshift("3");

var_dump($deq);

?>
```

**输出：**

```php
object(Ds\Deque)#1 (3) {
  [0]=>
  string(13) "GeeksforGeeks"
  [1]=>
  string(2) "to"
  [2]=>
  string(7) "Welcome"
}
object(Ds\Deque)#2 (8) {
  [0]=>
  string(1) "3"
  [1]=>
  string(1) "2"
  [2]=>
  string(1) "1"
  [3]=>
  string(1) "G"
  [4]=>
  string(1) "E"
  [5]=>
  string(1) "E"
  [6]=>
  string(1) "K"
  [7]=>
  string(1) "S"
}

```

**引用：**[https://www.php.net/manual/en/ds-deque.unshift.php](https://www.php.net/manual/en/ds-deque.unshift.php)