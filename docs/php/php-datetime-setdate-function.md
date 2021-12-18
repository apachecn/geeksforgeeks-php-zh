# PHP|DateTime setDate()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-setdate-function/](https://www.geeksforgeeks.org/php-datetime-setdate-function/)

**DateTime：：setDate()函数**是 PHP 中的一个内置函数，用于用给定的 Date-Time 对象重置 DateTime 对象的当前日期。

**语法：**

*   Object-oriented style:

    ```php
    *DateTime* DateTime::setDate( *int* $year, *int* $month, *int* $day )
    ```

*   Process style:

    ```php
    *DateTime* date_date_set( *DateTime* $object, *int* $year, *int* $month, *int* $day )
    ```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Year:** this parameter saves the annual value of the date.
*   **$Month:** this parameter holds the value of the month of the date.
*   **$day:** this parameter saves the date value of the date.

**返回值：**此函数成功时返回新的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DateTime：：setDate()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate
// DateTime::setDate() function

// Creating a new DateTime() object
$datetime = new DateTime();

// Initialising year, month and day
$Year = '2019';
$Month = '09';
$Day = '30';

// Calling the setDate() function
$datetime->setDate($Year, $Month, $Day);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $datetime->format('Y-m-d');
?>
```

**输出：**

```php
2019-09-30

```

**程序 2：**

```php
<?php
// PHP program to illustrate
// DateTime::setDate() function

// Creating a new DateTime() object
$datetime = new DateTime();

// Calling the setDate() function
// with parameters like years of 2019,
// month of 10 and day of 1
$datetime->setDate(2019, 10, 01);

// Getting a new set of date in the
// format of 'Y-m-d'
echo $datetime->format('Y-m-d');
?>
```

**输出：**

```php
2019-10-01

```

**引用：**[https://www.php.net/manual/en/datetime.setdate.php](https://www.php.net/manual/en/datetime.setdate.php)