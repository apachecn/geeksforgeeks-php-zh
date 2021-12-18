# PHP|DateTimeImmutable setDate()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-setdate-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-setdate-function/)

**DateTimeImmutable：：setDate()**函数是 PHP 中的内置函数，用于在创建的 DateTimeImmutable 对象中设置新日期。

**语法：**

```php
*DateTimeImmutable* DateTimeImmutable::setDate( *int* $year, *int* $month, *int* $day )

```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Year:** this parameter saves the annual value in integer format.
*   **$Month:** this parameter saves the month value in integer format.
*   **$day:** this parameter saves the date value in integer format.

**返回值：**此函数返回新的 Date 对象。

下面的程序演示了 PHP 中的**DateTimeImmutable：：setDate()**函数：

**程序 1：**

```php
<?php

// PHP program to illustrate DateTimeImmutable::setDate()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Initialising year, month and day
$Year = '2019';
$Month = '10';
$Day = '03';

// Calling the DateTimeImmutable::setDate() function
$a = $datetimeImmutable->setDate($Year, $Month, $Day);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

**输出：**

```php
2019-10-03

```

**程序 2：**

```php
<?php

// PHP program to illustrate DateTimeImmutable::setDate()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Calling the setDate() function
// with parameters like years of 2019,
// month of 10 and day of 3
$a = $datetimeImmutable->setDate(2019, 10, 03);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

**输出：**

```php
2019-10-03

```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.setdate.php](https://www.php.net/manual/en/datetimeimmutable.setdate.php)