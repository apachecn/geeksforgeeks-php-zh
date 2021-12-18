# PHP|DateTimeZone：：getName()函数

> Original: [https://www.geeksforgeeks.org/php-datetimezonegetname-function/](https://www.geeksforgeeks.org/php-datetimezonegetname-function/)

DateTimeZone：：getName()函数是 PHP 中的一个内置函数，用于返回创建的时区的名称。

**语法：**

```
DateTimeZone::getName()

```

**参数：**此函数不接受任何参数。

**返回值：**：此函数返回创建的时区名称。

以下程序说明了 DateTimeZone：：getName()函数：

**程序 1**：

```
<?php
// PHP program to illustrate DateTimeZone::getName()
// function

// Initialising a timezone
$timeZone = "Asia/Kolkata";

// Creating DateTimeZone() object with
// the above timezone
$DatetimeZone = new DateTimeZone($timeZone); 

// Getting the name of timezone  
print_r($DatetimeZone->getName()); 
?>
```

发帖主题：Re：Колибри0.7.0

```
Asia/Kolkata

```

**程序 2**：

```
<?php
// PHP program to illustrate DateTimeZone::getName()
// function

// Creating DateTimeZone() object with
// a specific timezone
$DatetimeZone = new DateTimeZone("Asia/Singapore"); 

// Getting the name of timezone  
print_r($DatetimeZone->getName()); 
?>
```

发帖主题：Re：Колибри0.7.0

```
Asia/Singapore

```

**参考**
[https://devdocs.io/php/datetimezone.getname](https://devdocs.io/php/datetimezone.getname)