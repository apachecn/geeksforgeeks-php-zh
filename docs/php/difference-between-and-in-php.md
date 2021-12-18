# 区别！== "和" ==！"在 PHP 中

> 原文:[https://www . geesforgeks . org/PHP 中的区别/](https://www.geeksforgeeks.org/difference-between-and-in-php/)

**！==运算符:**称为非相同运算符。如果操作数不相等，或者它们不是同一类型，则返回 true。

**语法:**

```
$x !== $y
```

其中$x 和$y 是操作数。

**==！符:**没什么但是可以进一步写成 **==(！操作数)**根据操作数返回真或假。这两个运算符都返回真或假的布尔值。

**语法:**

```
$x ==! $y
```

**示例:**

```
Input: $x = true
       $y = false
Operator: $x !== $y 
Output: true

Operator: $x ==! $y
Output: true

```

**示例 1:** 这个程序使用两个操作数并返回输出。

```
<?php
// PHP program to demonstrate
// !== and ==! operator

// Declare variables
$x = true;
$y = false;
$z = true;

// Using !== operator
echo "Using !== operator\n";

// Is $x not equals to $y
// so true returned
var_dump($x !== $y);

// Is $x not equals to $z
// so false returned
var_dump($x !== $z);

// Is $y not equals to $z
// so true returned
var_dump($y !== $z);

// Using ==! operator
echo "\nUsing ==! operator\n";

// Is $x equals to (!$y)
// so true returned
var_dump($x ==! $y);

// Is $x equals to (!$z)
// so false returned
var_dump($x ==! $z);

// Is $y equals to (!$z)
// so true returned
var_dump($y ==! $z);

?>
```

**Output:**

```
Using !== operator
bool(true)
bool(false)
bool(true)

Using ==! operator
bool(true)
bool(false)
bool(true)

```

**程序 2:**

```
<?php
// PHP program to demonstrate
// !== and ==! operator

// Dsclare associative array
$x = array(
    "1" => "Geeks", 
    "2" => "for",
    "3" => "Geeks"
);

$y = array(
    "5" => "Tony",
    "6" => "Captain",
    "7" => "Thor"
);

// Union of $x and $y
$z = $x + $y; 

// Using !== operator
echo "Using !== operator\n";

// Is $x not equals to $y
// so true returned
var_dump($x !== $y);

// Is $x not equals to $z
// so true returned
var_dump($x !== $z);

// Is $y not equals to $z
// so true returned
var_dump($y !== $z);

// Using ==! operator
echo "\nUsing ==! operator\n";

// Is $x equals to (!$y)
// so false returned
var_dump($x ==! $y);

// Is $x equals to (!$z)
// so false returned
var_dump($x ==! $z);

// Is $y equals to (!$z)
// so false returned
var_dump($y ==! $z);

?>
```

**Output:**

```
Using !== operator
bool(true)
bool(true)
bool(true)

Using ==! operator
bool(false)
bool(false)
bool(false)

```