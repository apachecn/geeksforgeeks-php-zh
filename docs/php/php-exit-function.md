# PHP|exit()函数

> Original: [https://www.geeksforgeeks.org/php-exit-function/](https://www.geeksforgeeks.org/php-exit-function/)

PHP 中的 exit()函数是一个内置函数，用于输出消息和终止当前脚本。
函数的作用是：只终止脚本的执行。 即使调用了 exit()函数，关机函数和对象析构函数也将始终执行。
要显示的消息作为参数传递给 exit()函数，它终止脚本并显示消息。
exit()函数是 die()函数的别名。

**语法：**

```php
exit(message)
```

**使用的参数：**
PHP 中的 exit()函数接受一个参数。

1.  Message：这是一个必选参数，用于指定退出脚本之前要写入的消息或状态号。

```php
Return Value:
It does not return any value.
```

**错误和异常**

1.  Exit()是一种语言构造，如果没有传递状态，则可以不带括号地调用它。
2.  如果作为参数传递的状态是整数，则该值将用作退出状态，不会打印。
3.  退出状态应该在 0 到 254 的范围内，不应该使用退出状态 255，因为它是由 PHP 保留的。

下面的程序说明了 exit()函数：

**程序 1：**

```php
<?php
$link = "https://www.geeksforgeeks.org";

// opening a link
fopen($link, "r")

//using exit() to display message and terminate script
or exit("Unable to establish a connection to $link");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Unable to establish a connection to https://www.geeksforgeeks.org

```

**程序 2：**

```php
<?php
//declaring variables
$a=5;
$b=5.0;

if($a==$b)
 {
    //terminating script with a message using exit()
    exit('variables are equal');
 }
else
 {
   //terminating script with a message using exit()
    exit('variables are not equal'); 
 }
?>
```

发帖主题：Re：Колибри0.7.0

```php
variables are equal

```

**引用：**
[http://php.net/manual/en/function.exit.php](http://php.net/manual/en/function.exit.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。