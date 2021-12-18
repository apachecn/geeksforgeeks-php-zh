# PHP|三元运算符

> Original: [https://www.geeksforgeeks.org/php-ternary-operator/](https://www.geeksforgeeks.org/php-ternary-operator/)

If-Else 和 Switch 用例用于评估条件和决定程序流。 三元运算符是用于缩短条件语句的快捷运算符。

**三元运算符：**三元运算符(？：)是一个条件运算符，用于对具有简单语句的条件执行简单比较或检查。 它缩短了执行条件运算的代码长度。 这个操作员的操作顺序是从左到右。 它之所以称为三元运算符，是因为它接受三个操作数-一个条件、一个 TRUE 的 RESULT 语句和一个 FALSE 的 RESULT 语句。 三元运算符的语法如下所示。

**语法：**

```php
(Condition) ? (Statement1) : (Statement2);
```

*   **condition:** it is the expression to be evaluated and returns a Boolean value.
*   **statement 1:** it is the statement to be executed when the conditional result is in the TRUE state.
*   **statement 2:** it is the statement to be executed when the condition causes a false state.

此比较的结果也可以使用赋值运算符赋给变量。 语法如下：

```php
Variable = (Condition) ? (Statement1) : (Statement2);
```

如果根据条件执行的语句返回任何值，则会将其赋给变量。

**三元运算符的优点：**以下是三元运算符的一些优点：

*   Using the ternary operator makes the code shorter than the if Else statement.
*   The length of this code is shorter than the if Else statement.
*   The readability of the code will be improved with the use of conditional statements.
*   The use of ternary operators makes the code easier.

**示例 1：**在此示例中，如果$a 的值大于 15，则返回 20 并将其分配给$b，否则将返回 5 并将其分配给$b。

## php

```php
<?php
  $a = 10;
  $b = $a > 15 ? 20 : 5;
  print ("Value of b is " . $b);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在本例中，如果$age 的值大于或等于 18，则将“Adult”传递给打印函数并打印，否则将传递并打印“Not Adult”。

## php

```php
<?php
  $age = 20;
  print ($age >= 18) ? "Adult" : "Not Adult";
?>
```

发帖主题：Re：Колибри0.7.8.0

**当我们使用三元运算符时：**当我们需要**简化 if-Else**语句时，我们使用三元运算符，这些语句只是根据条件为变量赋值。 使用三元运算符的一个优点是，它将巨大的 if-Else 块减少到一行，从而提高了代码的可读性并简化了代码。 在表单提交后分配变量时非常有用。

**示例：**

**原码：**和

## php

```php
<?php
if(isset($_POST['Name']))
    $name = $_POST['Name'];
else
    $name = null;

if(isset($_POST['Age']))
    $age = $_POST['Age'];
else
    $age = null;
?>
```

**简化为：**因此，三元运算符成功地将 if-Else 块减少到一行，从而达到其目的。

## php

```php
<?php
$name = isset($_POST['Name'])?$_POST['Name']:null;
$age = isset($_POST['Age'])?$_POST['Age']:null;
?>
```

(

## php

```php
<?php
$name = isset($_POST['Name'])?$_POST['Name']:null;
$age = isset($_POST['Age'])?$_POST['Age']:null;
?>
```

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。