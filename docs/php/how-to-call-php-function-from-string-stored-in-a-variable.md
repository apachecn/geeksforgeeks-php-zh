# 如何从变量

中存储的字符串调用 PHP 函数

> 原文:[https://www . geeksforgeeks . org/如何从字符串变量中调用 php 函数/](https://www.geeksforgeeks.org/how-to-call-php-function-from-string-stored-in-a-variable/)

给定一些以字符串形式存储在变量中的用户定义函数的名称。任务是使用存储在变量中的名称调用函数。

**例:**

```php
<?php

// Function without argument 
function func() {
    echo "geek";
}

// Function with argument
function fun($msg) {
    echo $msg;
}

// Call func and fun using $var and $var1
$var = "func";
$var1 = "fun";     
?>
```

有两种方法可以做到这一点。一种是通过使用括号和参数的变量名直接调用函数，另一种是通过使用 [call_user_func() Function](https://www.geeksforgeeks.org/php-call_user_func-function/) 调用函数，但是在这两种方法中都要使用变量名。

**程序:**

```php
<?php

// Function without argument 
function func() {
    echo "hello ";
}

// Function with argument
function fun($msg) {
    echo $msg." ";
}

$var = "func";
$var1 = "fun"; 

// 1st method by using variable name
$var();
$var1("geek");

echo "\n";

// 2nd method by using php inbuilt
// function call_user_func()
call_user_func($var);
call_user_func($var1, "fun_function"); 

?>
```

**输出:**

```php
hello geek 
hello fun_function

```