# PHP|ds\Set Join()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-join-function/](https://www.geeksforgeeks.org/php-dsset-join-function/)

**ds\set：：Join()**函数是 PHP 中的一个内置函数，用于将所有值连接为字符串。

**语法：**

```
*string* public Ds\Set::join ([ string $glue ] )

```

**参数：**此函数接受可选的单个参数**$glue**。 它用于分隔集合元素。

**返回值：**此函数返回字符串。

以下程序说明了 PHP 中的**ds\set：：Join()**函数：

**程序 1：**

```
<?php 

// Create new set
$set = new \Ds\Set(["G", "E", "E", 
                "K", "S", 1, 2, 3, 4]); 

// Use join() function and 
// display the string 
var_dump($set->join()); 

?> 
```

**输出：**

```
string(8) "GEKS1234"

```

**程序 2：**

```
<?php 

// Create new set
$set = new \Ds\Set(["G", "E", "E", 
                "K", "S", 1, 2, 3, 4]); 

// Use join() function and 
// display the string separated 
// with comma 
var_dump($set->join(", ")); 

// Create new set
$set = new \Ds\Set([1, 2, 3, "g", "e"]); 

// Use join() function 
var_dump($set->join("|")); 

?> 
```

**输出：**

```
string(22) "G, E, K, S, 1, 2, 3, 4"
string(9) "1|2|3|g|e"

```

**引用：**[https://www.php.net/manual/en/ds-set.join.php](https://www.php.net/manual/en/ds-set.join.php)