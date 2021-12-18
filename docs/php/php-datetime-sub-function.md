# PHP|datetime sub()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-sub-function/](https://www.geeksforgeeks.org/php-datetime-sub-function/)

**DateTime：：Sub()函数**是 PHP 中的一个内置函数，用于从创建的 DateTime 对象中减去若干天、月、年、小时、分钟和秒。

**语法：**

*   Object-oriented style:

    ```php
    *DateTime* DateTime::sub( *DateInterval* interval )
    ```

*   Process style:

    ```php
    *DateTime* date_sub( *DateTime* $object, *DateInterval* $interval )
    ```

**参数：**此函数使用上述两个参数，如下所述：

*   **$object:** this parameter holds the DateTime object created by the date_create () function.
*   **$Interval:** this parameter saves the DateInterval object.

**返回值：**此函数成功时返回减法后的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DateTime：：Sub()函数：

**程序 1：**此程序使用 DateTime：：Sub()函数从给定的日期对象中减去 2 天。

```php
<?php

// PHP program to illustrate DateTime::sub()
// function

// Creating a new DateTime() object
$datetime = new DateTime('2019-10-03');

// Initialising a interval of 2 days
$interval = 'P2D';

// Calling the sub() function
$datetime->sub(new DateInterval($interval));

// Getting a new date time
// format of 'Y-m-d'
echo $datetime->format('Y-m-d');
?>
```

**输出：**

```php
2019-10-01

```

**程序 2：**此程序使用 DateTime：：Sub()函数从 Date 对象中减去给定的间隔。

```php
<?php
// PHP program to illustrate DateTime::sub()
// function

// Creating a new DateTime() object
$datetime = new DateTime('2019-10-03');

// Initialising an interval
$interval = 'P2Y5M2DT0H30M40S';

// Calling the sub() function
$datetime->sub(new DateInterval($interval));

// Getting a new date time
// format of 'Y-m-d H:i:s'
echo $datetime->format('Y-m-d H:i:s');

?>
```

**输出：**

```php
2017-04-30 23:29:20

```

**引用：**[https://www.php.net/manual/en/datetime.sub.php](https://www.php.net/manual/en/datetime.sub.php)