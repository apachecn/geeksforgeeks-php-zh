# PHP|ds\set diff()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-diff-function/](https://www.geeksforgeeks.org/php-dsset-diff-function/)

**ds\set：：diff()**函数是 PHP 中的一个内置函数，用于创建包含第一个集合中不存在于第二个集合中的元素的集合。

**语法：**

```
*Ds\Set* public Ds\Set::diff ( Ds\Set $set )

```

**参数：**用于保存集合，需要排除的值。

**返回值：**它返回一个新集合，其中包含第一个集合中不存在于第二个集合中的元素。

以下程序说明了 PHP 中的**ds\set：：diff()**函数：

**程序 1：**

```
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6]); 

// Declare another new set
$b = new \Ds\Set([2, 4, 6, 7]); 

// Print the diff of set
echo("Difference of set1 and set2: \n"); 

print_r($a->diff($b));

?>
```

**输出：**

```
Difference of set1 and set2: 
Ds\Set Object
(
    [0] => 3
)

```

**程序 2：**

```
<?php 

// Declare a new set
$a = new \Ds\Set([2, 3, 6, 7, 8]); 

// Declare another new set
$b = new \Ds\Set([2, 3, 5, 8, 9, 10]); 

// Print the diff of set
echo("Difference of set1 and set2: \n"); 

var_dump($a->diff($b));

?>
```

**输出：**

```
Difference of set1 and set2: 
object(Ds\Set)#3 (2) {
  [0]=>
  int(6)
  [1]=>
  int(7)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.diff.php](https://www.php.net/manual/en/ds-set.diff.php)