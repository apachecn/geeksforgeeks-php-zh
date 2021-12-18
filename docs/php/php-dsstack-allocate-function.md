# PHP|ds\堆栈分配()函数

> Original: [https://www.geeksforgeeks.org/php-dsstack-allocate-function/](https://www.geeksforgeeks.org/php-dsstack-allocate-function/)

**ds\Stack：：Allocation()函数**是 PHP 中的一个内置函数，用于为所需的容量分配内存。 此函数为 Stack 类实例的给定容量分配足够的内存。
**语法：**和

```php
*void* Ds\Stack::allocate( $capacity )
```

**参数：**此函数接受单个参数**$Capacity**，该参数是一个整数值，表示需要分配容量的值的数量。
**返回值：**此函数不返回任何值。
下面的程序说明了 PHP：
**程序 1：**和
中的 Ds\Stack：：Allocation()函数

## PHP

```php
<?php

// PHP program to illustrate the
// Ds\Stack::allocate() function

// Create a Stack instance
$stack = new \Ds\Stack();

echo("Allocated Space is: ");

// Use capacity() function
var_dump($stack->capacity());

echo("Allocated space is: ");

// Use allocate() function to 
// allocate capacity
$stack->allocate(50);

// Display the allocated stack
// capacity
var_dump($stack->capacity());

?>
```

**Output:** 

```php
Allocated Space is: int(8)
Allocated space is: int(50)
```

**程序 2：**和

## PHP

```php
<?php

// Declare new stack
$stack = new \Ds\Stack();

echo("Allocated Space is: ");

// Use capacity() function
var_dump($stack->capacity());

echo("Allocated space is: ");

// Use allocate() function to
// allocate capacity
$stack->allocate(5);

// Display the stack capacity
var_dump($stack->capacity());

echo("Allocated space is: ");

// Use allocate() function to
// allocate capacity
$stack->allocate(120);

// Display the stack capacity
var_dump($stack->capacity());
?>
```

**Output:** 

```php
Allocated Space is: int(8)
Allocated space is: int(8)
Allocated space is: int(120)
```

**引用：**[https://www.php.net/manual/en/ds-stack.allocate.php](https://www.php.net/manual/en/ds-stack.allocate.php)