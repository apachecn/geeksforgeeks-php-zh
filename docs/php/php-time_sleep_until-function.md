# PHP|TIME_SLEEP_Until()函数

> Original: [https://www.geeksforgeeks.org/php-time_sleep_until-function/](https://www.geeksforgeeks.org/php-time_sleep_until-function/)

PHP 中的 TIME_SLEEP_Until()函数是一个内置函数，用于将当前脚本的执行延迟到指定的时间。
函数的作用是：接受 TIMESTAMP 作为参数，这个 TIMESTAMP 表示脚本应该在什么时候唤醒。
函数的作用是：成功时返回 TRUE，失败时返回 FALSE。

**语法：**

```php
time_sleep_until(timestamp)
```

**使用的参数：**PHP 中的 TIME_SLEEP_Until()函数接受一个参数*时间戳*。 这是指定唤醒时间的必选参数。

**返回值：**成功返回 TRUE，失败返回 FALSE。

**错误和异常**：

1.  如果指定的时间戳是过去时间，此函数将生成 E_WARNING。
2.  所有信号都是在脚本唤醒后发送的。
3.  如果指定的数字为负数，此函数将引发错误。

**示例：**

```php
Input : echo date('h:i:s');
        time_sleep_until(time()+5);
        echo date('h:i:s'); 
Output: 07:23:26
        07:23:31

Input : echo date('h:i:s');
        time_sleep_until(time()+ rand(1, 3));
        echo date('h:i:s');
Output : 07:21:55
         07:21:57

```

下面的程序举例说明了 TIME_SLEEP_Until()函数：

**程序 1**：

```php
<?php
// displaying time
echo date('h:i:s');

// delaying execution of script for 5 seconds
time_sleep_until(time()+5);

// displaying time again
echo ("\n");
echo date('h:i:s'); 
?>
```

**Output:**

```php
06:50:04
06:50:08

```

**程序 2**：

```php
<?php
// displaying time
echo date('h:i:s');

// using rand() function to randomly choose a
// value and delay execution of the script
time_sleep_until(time()+ rand(1, 3));

// displaying time again
echo ("\n");
echo date('h:i:s'); 
?>
```

**Output:**

```php
06:50:14
06:50:15

```

**程序 3**：

```php
<?php

// delaying execution of script with negative time
time_sleep_until(time()-2);

// displaying time again
echo ("\n");
echo date('h:i:s'); 
?>
```

**Output:**

```php
false

```

**引用：**[http://php.net/manual/en/function.time-sleep-until.php](http://php.net/manual/en/function.time-sleep-until.php)