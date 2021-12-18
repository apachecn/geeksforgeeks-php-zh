# PHP|ds\set Union()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-union-function/](https://www.geeksforgeeks.org/php-dsset-union-function/)

**ds\set：：Union()**函数是 PHP 中的一个内置函数，用于创建包含两个集合的并集的新集合。

**语法：**

```php
*Ds\Set* public Ds\Set::union ( Ds\Set $set )

```

**参数：**此函数接受单个参数**$set**，该参数保存要与当前实例组合的另一组实例。

**返回值：**它返回一个包含两个集合的并的集合。

下面的程序说明了 PHP 中的**ds\set：：Union()**函数：

**程序 1：**

```php
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6]); 

// Declare another new set
$b = new \Ds\Set([2, 4, 6, 7]); 

// Print the Union of both set
echo("Union of both set is: \n"); 

print_r($a->union($b));

?>
```

**输出：**

```php
Union of both set is: 
Ds\Set Object
(
    [0] => 2
    [1] => 3
    [2] => 6
    [3] => 4
    [4] => 7
)

```

**程序 2：**

```php
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6, 7, 8]); 

// Declare another new set
$b = new \Ds\Set([2, 3, 5, 8, 9, 10]); 

// Print the union of both set
echo("Union of both set is: \n"); 

var_dump($a->union($b));

?>
```

**输出：**

```php
Union of both set is: 
object(Ds\Set)#3 (8) {
  [0]=>
  int(2)
  [1]=>
  int(3)
  [2]=>
  int(6)
  [3]=>
  int(7)
  [4]=>
  int(8)
  [5]=>
  int(5)
  [6]=>
  int(9)
  [7]=>
  int(10)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.union.php](https://www.php.net/manual/en/ds-set.union.php)