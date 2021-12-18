# 如何在 PHP 中显示数组结构和值？

> 原文:[https://www . geesforgeks . org/how-display-array-structure-and-values-in-PHP/](https://www.geeksforgeeks.org/how-to-display-array-structure-and-values-in-php/)

在本文中，我们将讨论如何在 PHP 中显示数组结构和值。要显示数组结构及其值，我们可以使用**[<u>var _ dump()</u>](https://www.geeksforgeeks.org/php-var_dump-function/)和 [<u>print_r()</u>](https://www.geeksforgeeks.org/php-print_r-function/#:~:text=The%20print_r()%20function%20is,information%20stored%20in%20a%20variable.&text=Parameters%3A%20This%20function%20accepts%20two,and%20is%20a%20mandatory%20parameter.) 功能。**

**它包括**

*   **数组大小**
*   **数组值**
*   **带索引的数组值**
*   **每种数值数据类型**

**我们将使用**[***<u>var _ dump()</u>***](https://www.geeksforgeeks.org/php-var_dump-function/)功能显示阵列结构。此功能用于转储关于变量的信息。该功能显示给定变量的类型和值等结构化信息。数组和对象被递归探索，其值缩进以显示结构。这个函数对表达式也是有效的。****

******语法:******

```php
**var_dump( $array_name )**
```

******参数:** 该函数采用单个参数 $array_name ，该参数可以是一个单变量或包含多个任意类型的空格分隔的变量的表达式。****

******返回类型:**数组结构****

******示例:**创建数组并显示其结构的 PHP 程序。****

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```php
**<?php

// Array with subjects
$array1 = array(
      '0' => "Python", 
      '1' => "java", 
      '2' => "c/cpp"
);

// Display array structure
var_dump($array1);

?>**
```

******Output**

```php
array(3) {
  [0]=>
  string(6) "Python"
  [1]=>
  string(4) "java"
  [2]=>
  string(5) "c/cpp"
}

```**** 

****在这里，****

*   ****array(3)是数组(3 个元素)的大小****
*   ****字符串(6)是元素 1 的数据类型及其大小****
*   ****字符串(4)是元素 2 的数据类型及其大小****
*   ****字符串(5)是元素 3 的数据类型及其大小****

******数组值:**我们将使用[***<u>print _ r()</u>***](https://www.geeksforgeeks.org/php-print_r-function/#:~:text=The%20print_r()%20function%20is,information%20stored%20in%20a%20variable.&text=Parameters%3A%20This%20function%20accepts%20two,and%20is%20a%20mandatory%20parameter.)功能显示数组值。此功能用于打印或显示变量中存储的信息。****

******语法:******

```php
**print_r( $variable, $isStore )**
```

******参数:******

*   ******$变量**:该参数指定了要打印的变量，是必选参数。****
*   ******$isStore** :这是可选参数。此参数为布尔类型，默认值为 FALSE，用于将 print_r()函数的输出存储在变量中，而不是将其打印出来。如果该参数设置为真，那么 print_r()函数将返回它应该打印的输出。****

******返回值:**带值数组。****

******示例:**显示一组值的 PHP 程序。****

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```php
**<?php

// Array with subjects
$array1 = array(
      '0' => "Python", 
      '1' => "java", 
      '2' => "c/cpp"
);

// Display array values
print_r($array1);

?>**
```

******Output**

```php
Array
(
    [0] => Python
    [1] => java
    [2] => c/cpp
)

```****