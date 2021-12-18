# PHP|Ds\Vector__Construction()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-__construct-function/](https://www.geeksforgeeks.org/php-dsvector-__construct-function/)

**ds\Vector：：__Construction()**函数是 PHP 中的内置函数，用于创建新实例。

**语法：**

```
public Ds\Vector::__construct( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要使用初始值的可遍历对象或数组。

下面的程序说明了 PHP 中的**ds\Vector：：__Construction()**函数：

**程序 1：**

```
<?php 

// Declare a new Vector
$vect = new \Ds\Vector();
print_r($vect);

// Declare a new set
$vect = new \Ds\Vector(['G', 'E', 'K', 'S']); 
print_r($vect);

?>
```

**Output:**

```
Ds\Vector Object
(
)
Ds\Vector Object
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

// Declare a new vector
$vect = new \Ds\Vector([2, 3, 6, 7, 8]); 
var_dump($vect);

// Declare a new vector
$vect = new \Ds\Vector([2, 3, 5, 8, 9, 10]); 
var_dump($vect);
?>
```

**输出：**

```
object(Ds\Vector)#1 (5) {
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
object(Ds\Vector)#2 (6) {
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

**引用：**[https://www.php.net/manual/en/ds-vector.construct.php](https://www.php.net/manual/en/ds-vector.construct.php)