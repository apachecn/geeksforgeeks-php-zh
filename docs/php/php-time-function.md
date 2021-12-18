# PHP|time()函数

> Original: [https://www.geeksforgeeks.org/php-time-function/](https://www.geeksforgeeks.org/php-time-function/)

Time()函数是 PHP 中的一个内置函数，它返回从[Unix Epoch](https://en.wikipedia.org/wiki/Unix_time)开始以秒为单位测量的当前时间。 可以使用 PHP 中的 date()函数将秒数转换为当前日期。

**语法：**

```php
*int* time()
```

**参数：**此函数不接受如上所示的任何参数。

**返回值：**此函数返回自[Unix 纪元以来的当前时间(以秒为单位)。](https://en.wikipedia.org/wiki/Unix_time)

**注意：**程序的所有输出都与文章的撰写日期相对应。

以下程序说明了 time()函数：

**程序 1：**下面的程序以秒为单位打印当前时间。

```php
<?php
// PHP program to demonstrate the use of current 
// time in seconds since Unix Epoch 

// variable to store the current time in seconds 
$currentTimeinSeconds = time(); 

// prints the current time in seconds
echo $currentTimeinSeconds; 
?>
```

帖子主题：Re：Колибри

**程序 2：**下面的程序以日期格式打印当前时间。

```php
<?php
// PHP program to demonstrate the use of current 
// date since Unix Epoch 

// variable to store the current time in seconds 
$currentTimeinSeconds = time(); 

// converts the time in seconds to current date 
$currentDate = date('Y-m-d', $currentTimeinSeconds);

// prints the current date
echo ($currentDate); 
?>
```

帖子主题：Re：Колибри