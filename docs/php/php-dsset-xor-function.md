# PHP|ds\set xor()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-xor-function/](https://www.geeksforgeeks.org/php-dsset-xor-function/)

**ds\set：：XOR()**函数是 PHP 中的一个内置函数，用于创建一个新的集合，该集合包含第一个集合或第二个集合中的值，但不能同时包含这两个集合中的值。

**语法：**

```php
*Ds\Set* public Ds\Set::xor ( Ds\Set $set )

```

**参数：**此函数接受单个参数**$set**，该参数用于保存值集合。

**返回值：**返回一个集合，该集合包含当前集合与另一个集合的 XOR。

下面的程序说明了 PHP 中的**ds\set：：XOR()**函数：

**程序 1：**

```php
<?php 

// Declare a new set
$a = new \Ds\Set([1, 3, 5]); 

// Declare a new set
$b = new \Ds\Set([2, 3, 6]); 

// Print the xor of both set
echo("xor of both set is: \n"); 

print_r($a->xor($b));

?>
```

**输出：**

```php
xor of both set is: 
Ds\Set Object
(
    [0] => 1
    [1] => 5
    [2] => 2
    [3] => 6
)

```

**程序 2：**

```php
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6, 7, 8]); 

// Declare a new set
$b = new \Ds\Set([2, 3, 5, 8, 9, 10]); 

// Print the xor of both set
echo("xor of both set is: \n"); 

var_dump($a->xor($b));

?>
```

**输出：**

```php
xor of both set is: 
object(Ds\Set)#3 (5) {
  [0]=>
  int(6)
  [1]=>
  int(7)
  [2]=>
  int(5)
  [3]=>
  int(9)
  [4]=>
  int(10)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.xor.php](https://www.php.net/manual/en/ds-set.xor.php)