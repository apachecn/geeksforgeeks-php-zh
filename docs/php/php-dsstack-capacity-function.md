# PHP|ds\Stack Capacity()函数

> Original: [https://www.geeksforgeeks.org/php-dsstack-capacity-function/](https://www.geeksforgeeks.org/php-dsstack-capacity-function/)

**ds\Stack：：Capacity()函数**是 PHP 中的内置函数，用于返回堆栈的当前容量。

**语法：**

```php
*int* Ds\Stack::capacity( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回堆栈的当前容量。

以下程序说明了 PHP 中的 ds\Stack：：Capacity()函数：

**程序 1：**

```php
<?php 

// Declare new Stack 
$stack = new \Ds\Stack(); 

// Use capacity() function to check
// the current capacity 
var_dump($stack->capacity()); 

?>
```

**输出：**

```php
int(8)

```

**程序 2：**

```php
<?php 

// Declare new Stack 
$stack = new \Ds\Stack(); 

echo("Current Capacity is: "); 

// Use capacity() function 
// to check the current capacity 
var_dump($stack->capacity()); 

echo("Current Capacity is: "); 

// Use allocate() function to 
// allocate capacity 
$stack->allocate(5); 

// Display the allocated vector 
// capacity 
var_dump($stack->capacity()); 

echo("Current Capacity is: ");

// Use allocate() function to 
// allocate capacity 
$stack->allocate(120); 

// Display the allocated vector 
// capacity 
var_dump($stack->capacity()); 

?> 
```

**输出：**

```php
Current Capacity is: int(8)
Current Capacity is: int(8)
Current Capacity is: int(120)

```

**引用：**[https://www.php.net/manual/en/ds-stack.capacity.php](https://www.php.net/manual/en/ds-stack.capacity.php)