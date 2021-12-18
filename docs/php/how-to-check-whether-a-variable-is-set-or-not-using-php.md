# 如何用 PHP 检查一个变量是否设置？

> 原文:[https://www . geeksforgeeks . org/如何检查变量是否使用 php 设置/](https://www.geeksforgeeks.org/how-to-check-whether-a-variable-is-set-or-not-using-php/)

我们给了一个变量，任务是检查 PHP 中是否设置了一个变量**var**。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用**[**isset****()方法**](https://www.geeksforgeeks.org/php-isset-function/)**:****isset****()**方法 如果变量被声明且其值不等于 NULL，则返回 **True** 。

**语法:**

```php
*bool* isset( *mixed* $var [, *mixed* $... ] )

```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to check whether 
// a variable is set or not 

$str = "GeeksforGeeks"; 

// Check value of variable is set or not 
if(isset($str)) { 
    echo "Value of variable is set"; 
} 
else { 
    echo "Value of variable is not set"; 
} 
?> 
```

**Output**

```php
Value of variable is set 

```