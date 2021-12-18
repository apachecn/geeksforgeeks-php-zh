# PHP|DS\SET INTERSECT()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-intersect-function/](https://www.geeksforgeeks.org/php-dsset-intersect-function/)

**ds\set：：intersect()**函数是 PHP 中的一个内置函数，用于创建包含两个集合的交集的新集合。

**语法：**

```
*Ds\Set* public Ds\Set::intersect ( Ds\Set $set )

```

**参数：**此参数保存包含集合元素的集合。

**返回值：**此函数返回当前集合与其他集合的交集。

下面的程序说明了 PHP 中的**ds\set：：intersect()**函数：

**程序 1：**

```
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6]); 

// Declare another new set
$b = new \Ds\Set([2, 4, 6, 7]); 

// Print the Intersection of two set
echo("Intersection of both set is: \n"); 

print_r($a->intersect($b));

?>
```

**输出：**

```
Intersection of both set is: 
Ds\Set Object
(
    [0] => 2
    [1] => 6
)

```

**程序 2：**

```
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6, 7, 8]); 

// Declare another set
$b = new \Ds\Set([2, 3, 5, 8, 9, 10]); 

// Print the Intersection of both set
echo("Intersection of both set is: \n"); 

var_dump($a->intersect($b));

?>
```

**输出：**

```
Intersection of both set is: 
object(Ds\Set)#3 (3) {
  [0]=>
  int(2)
  [1]=>
  int(3)
  [2]=>
  int(8)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.intersect.php](https://www.php.net/manual/en/ds-set.intersect.php)