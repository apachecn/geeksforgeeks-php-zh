# PHP|usleep()函数

> Original: [https://www.geeksforgeeks.org/php-usleep-function/](https://www.geeksforgeeks.org/php-usleep-function/)

PHP 中的 usleep()函数是一个内置函数，用于将当前脚本的执行延迟特定的微秒。 它与将当前脚本的执行延迟指定秒数的 SLEEP()函数类似，而与将当前脚本的执行延迟指定微秒数的 usleEP()函数不同。 微秒数作为参数传递给 usleEP 函数，它根据作为参数传递的上述延迟来执行脚本。

**语法：**

```
usleep(microseconds)
```

**使用的参数：**PHP 中的 usule()函数接受一个参数*微秒*。 这是一个必选参数，用于指定脚本执行的延迟时间。

**返回值：**不返回任何值。

**错误和异常**：

1.  函数的作用是：如果指定的秒数为负数，则抛出错误。
2.  Usleepth()函数调用消耗 CPU 周期，只有在必要时才能使用。 SLEEP()函数是一个更好的选择，因为它不占用 CPU 周期。

**示例：**

```
Input : echo date('h:i:s');
        usleep(2000000);
        echo date('h:i:s');

Output : 06:53:48
         06:53:50

Input : echo date('h:i:s');
        usleep(rand(1000000, 5000000))
        echo date('h:i:s');

Output : 06:53:48
         06:53:52

```

下面的程序说明了 usleEP()函数：

**程序 1**：

```
<?php
// displaying time
echo date('h:i:s') ;

// delaying execution of script for 2 seconds
usleep(2000000);

// displaying time again
echo date('h:i:s');
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2**：

```
<?php
// displaying time
echo date('h:i:s') ;

// using rand() function to randomly choose a
// value and delay execution of the script
usleep(rand(1000000, 5000000))

// displaying time again
echo date('h:i:s');
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.usleep.php](http://php.net/manual/en/function.usleep.php)