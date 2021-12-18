# PHP|ds\Stack Count()函数

> Original: [https://www.geeksforgeeks.org/php-dsstack-count-function/](https://www.geeksforgeeks.org/php-dsstack-count-function/)

**ds\Stack：：Count()函数**是 PHP 中的一个内置函数，用于计算 Stack 中存在的元素数量。

**语法：**

```php
*int* Ds\Stack::count( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回堆栈中存在的元素数。

下面的程序说明了 PHP 中的 Ds\Stack：：Count()函数：

**程序 1：**

```php
<?php 

// Declare new stack 
$stack = new \Ds\Stack([10, 15, 21]); 

// Display the stack element 
var_dump($stack); 

// Count number of elements 
// present in the stack 
echo "Number of elements present in the stack: "; 
print_r($stack->count()); 

?> 
```

**输出：**

```php
object(Ds\Stack)#1 (3) {
  [0]=>
  int(21)
  [1]=>
  int(15)
  [2]=>
  int(10)
}
Number of elements present in the stack: 3

```

**程序 2：**

```php
<?php 

// Declare new stack 
$stack = new \Ds\Stack(["Geeks", "for", "Keegs"]); 

// Display the stack element 
print_r($stack); 

// Display count of elements 
// present in the stack 
echo "Number of elements present in the stack: "; 
var_dump($stack->count()); 

?> 
```

**输出：**

```php
Ds\Stack Object
(
    [0] => Keegs
    [1] => for
    [2] => Geeks
)
Number of elements present in the stack: int(3)

```

**引用：**[https://www.php.net/manual/en/ds-stack.count.php](https://www.php.net/manual/en/ds-stack.count.php)