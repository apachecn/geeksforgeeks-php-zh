# PHP|ds\set__struct()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-__construct-function/](https://www.geeksforgeeks.org/php-dsset-__construct-function/)

**ds\set：：__struct()**函数是 PHP 中的内置函数，用于创建 Set 的新实例。

**语法：**

```
Ds\Set::__construct( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要使用初始值的可遍历对象或数组。

下面的程序说明了 PHP 中的**ds\set：：__struct()**函数：

**程序 1：**

```
<?php 

// Declare a new set
$set = new \Ds\Set();
print_r($set);

// Declare a new set
$set = new \Ds\Set(['G', 'E', 'K', 'S']); 
print_r($set);

?>
```

**Output:**

```
Ds\Set Object
(
)
Ds\Set Object
(
    [0] => G
    [1] => E
    [2] => K
    [3] => S
)

```

**程序 2：**

```
<?php 

// Declare a new set
$set = new \Ds\Set([2, 3, 6, 7, 8]); 
var_dump($set);

// Declare a new set
$set = new \Ds\Set([2, 3, 5, 8, 9, 10]); 
var_dump($set);
?>
```

**输出：**

```
object(Ds\Set)#1 (5) {
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
}
object(Ds\Set)#2 (6) {
  [0]=>
  int(2)
  [1]=>
  int(3)
  [2]=>
  int(5)
  [3]=>
  int(8)
  [4]=>
  int(9)
  [5]=>
  int(10)
}

```

**引用：**[https://www.php.net/manual/en/ds-set.construct.php](https://www.php.net/manual/en/ds-set.construct.php)