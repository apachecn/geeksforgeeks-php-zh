# 交换两个数字

的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-to-swap-two-numbers/](https://www.geeksforgeeks.org/php-program-to-swap-two-numbers/)

在 PHP 中，整数值可以存储在变量中。 使用上述各种方法很容易存储、修改和交换这些整数值：

**使用临时变量：**第一个数字的值存储在临时变量中。 然后，该值将被第二个数字的值替换。 然后将临时变量的值赋给第二个数字。 执行此操作所需的时间复杂度为 O(1)。 所需空间也大致相当于 O(1)。

## PHP

```
<?php

// Declaring both the numbers
$num1 = 9;
$num2 = 4;
print ("Number 1 original: " . $num1 . "</br>");
print ("Number 2 original: " . $num2 . "</br>");

// Assigning num1 value to temp variable
$temp_num = $num1;

// Assigning num1 value to num2
$num1 = $num2;

// Assigning num2 value to temp num
$num2 = $temp_num;
print ("Number 1 modified: " . $num1 . "</br>");
print ("Number 2 modified: " . $num2 . "</br>");
?> 
```

发帖主题：Re：Колибри0.7.0

```
Number 1 original: 9
Number 2 original: 4
Number 1 modified: 4
Number 2 modified: 9
```

**使用^运算符：**XOR 运算符可用于在 PHP 中交换数字。 但是，此技术仅适用于整数的情况。 XOR 运算符应用程序需要恒定的时间复杂度和空间复杂度。

## PHP

```
<?php

// Declaring both the numbers
$num1 = 9;
$num2 = 4;
print ("Number 1 original: " . $num1 . "</br>");
print ("Number 2 original: " . $num2 . "</br>");

// Swapping numbers
$num1 ^= $num2 ^= $num1 ^= $num2;
print ("Number 1 modified: " . $num1 . "</br>");
print ("Number 2 modified: " . $num2 . "</br>");

?>
```

发帖主题：Re：Колибри0.7.0

```
Number 1 original: 9
Number 2 original: 4
Number 1 modified: 4
Number 2 modified: 9
```

**使用 array()方法：**使用参数作为交换后的数字创建数组对象，即第一个参数是第二个数字，第二个参数是第一个数字。

**语法：**

```
array(num2 , num1)
```

**示例：**然后使用 list()方法将其分配给列表对象，按顺序存储数字，即第一个数字后跟第二个数字。 这将交换数字。 但是，此方法仅适用于整数。

## PHP

```
<?php

// Declaring both the numbers
$num1 = 9;
$num2 = 4;
print ("Number 1 original: " . $num1 . "</br>");
print ("Number 2 original: " . $num2 . "</br>");

// Swapping numbers
list($num1, $num2) = array($num2, $num1);
print ("Number 1 modified: " . $num1 . "</br>");
print ("Number 2 modified: " . $num2 . "</br>")

?>
```

发帖主题：Re：Колибри0.7.0

```
Number 1 original: 9
Number 2 original: 4
Number 1 modified: 4
Number 2 modified: 9
```