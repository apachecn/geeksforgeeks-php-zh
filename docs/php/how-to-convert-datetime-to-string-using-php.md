# 如何用 PHP 把 DateTime 转换成 String？

> 原文:[https://www . geesforgeks . org/如何使用-php 将-datetime 转换为字符串/](https://www.geeksforgeeks.org/how-to-convert-datetime-to-string-using-php/)

任务是使用 PHP 将日期时间转换为字符串。有两种方法可以转换它。

#### **1。通过使用[格式方法](https://www.geeksforgeeks.org/php-datetime-format-function/)**

*   在 Format 方法中，我们可以将 DateTime 对象转换为字符串。
*   日期时间到字符串程序编程如下:

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Store datetime in variable today
$today = date("d/m/Y H:i:s");    

if ($today) { 
    echo $today; 

// If unknown time 
} else {  
    echo "can't display time"; 
}
?>
```

**输出:**

```
07/05/2021 17:57:38

```

**2。通过使用[列表()方法:](https://www.geeksforgeeks.org/php-list-function/)**

*   list()方法用于将 DateTime 对象转换为字符串。
*   列表方法的较短方式如下:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?PHP

// Using list method to display the datetime
list($day, $month, $year, $hour, $min, $sec) 
        = explode("/", date('d/m/Y/h/i/s')); 

// Display the datetime
echo $month . '/' . $day . '/' . $year . ' '
    . $hour . ':' . $min . ':' . $sec;

?>
```

**输出:**

```
05/07/2021 05:58:48
```