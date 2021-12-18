# PHP|DateTimeImmutable setISODate()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-setisodate-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-setisodate-function/)

**DateTimeImmutable：：setISODate()**函数是 PHP 中的内置函数，用于将 ISO(国际标准化组织)日期设置到创建的 DateTimeImmutable 对象中。 此函数根据 ISO 8601 标准设置日期，使用周和日偏移量而不是特定日期。

**语法：**

```
*DateTimeImmutable* DateTimeImmutable::setISODate( *int* year, *int* week, *int* day) )

```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **Year:** this parameter saves the annual value in integer format.
*   **week:** this parameter saves the week value in integer format.
*   **day:** this parameter saves the value of the day in integer format.

**返回值：**此函数返回新日期。

下面的程序说明了 PHP 中的**DateTimeImmutable：：setISODate()**函数：

**程序 1：**

```
<?php
// PHP program to illustrate DateTimeImmutable::setISODate()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Initialising year, week and day
$Year = '2019';
$Week = '10';
$Day = '03';

// Calling the DateTimeImmutable::setISODate() function
$a = $datetimeImmutable->setISODate($Year, $Week, $Day);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
// PHP program to illustrate DateTimeImmutable::setISODate()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Calling the setISODate() function
// with parameters like years of 2019,
// week of 9 and day of 3
$a = $datetimeImmutable->setISODate(2019, 9, 03);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/datetimeimmutable.setisodate.php](https://www.php.net/manual/en/datetimeimmutable.setisodate.php)