# PHP|DateTimeImmutable：：setTimezone()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutablesettimezone-function/](https://www.geeksforgeeks.org/php-datetimeimmutablesettimezone-function/)

DateTimeImmutable：：setTimezone()函数是 PHP 中的一个内置函数，用于为创建的 DateTimeImmutable 对象设置时区。 此函数返回 DateTimeImmutable 对象，如果失败则返回 False。

**语法：**

```php
DateTimeImmutable::setTimezone ( TimeZone )

```

**参数：**此函数接受一个参数，如下图所示：-

```php
TimeZone: This parameter is used to set the DateTimeZone object representing the desired time zone.

```

**返回值**：此函数成功时返回 DateTimeImmutable 对象，失败时返回 False。

以下程序说明了 DateTimeImmutable：：setTimezone()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate DateTimeImmutable::setTimezone()
// function

// Creating a DateTimeImmutable() object 
$DateTimeImmutable = new DateTimeImmutable('2019-10-07', new DateTimeZone('Asia/Kolkata')); 

// Getting the above datetime format 
echo $DateTimeImmutable->format('d-m-Y H:i:sP') . "\n"; 

// Calling the DateTimeImmutable::setTimezone() function
$a = $DateTimeImmutable->setTimezone(new DateTimeZone('Asia/Singapore')); 

// Getting a new DateTimeImmutable object
echo $a->format('d-m-Y H:i:sP'); 
?>
```

发帖主题：Re：Колибри0.7.0

```php
07-10-2019 00:00:00+05:30
07-10-2019 02:30:00+08:00

```

**程序 2**：

```php
<?php
// PHP program to illustrate DateTimeImmutable::setTimezone()
// function

// Creating a DateTimeImmutable() object 
$DateTimeImmutable = new DateTimeImmutable('2019-10-07'); 

// Getting the above datetime format 
echo $DateTimeImmutable->format('d-m-Y H:i:sP') . "\n"; 

// Calling the DateTimeImmutable::setTimezone() function
$a = $DateTimeImmutable->setTimezone(new DateTimeZone('Asia/Singapore')); 

// Getting a new DateTimeImmutable object
echo $a->format('d-m-Y H:i:sP'); 
?>
```

发帖主题：Re：Колибри0.7.0

```php
07-10-2019 00:00:00+00:00
07-10-2019 08:00:00+08:00

```

**引用：**
[https://devdocs.io/php/datetimeimmutable.settimezone](https://devdocs.io/php/datetimeimmutable.settimezone)