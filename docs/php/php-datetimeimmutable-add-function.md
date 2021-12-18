# PHP|DateTimeImmutable add()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-add-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-add-function/)

**DateTimeImmutable：：add()函数**是 PHP 中的一个内置函数，用于将若干天、月、年、小时、分钟和秒添加到创建的 DateTimeImmutable 对象中。

**语法：**

```
*DateTimeImmutable* DateTimeImmutable::add( *DateInterval* $interval )
```

**参数：**此函数接受单个参数**$interval**，该参数保存要添加到给定 DateTimeImmutable 对象的天数、月数、年数、小时数、分钟数或秒数。

**返回值：**此函数在加法后返回最终的 DateTimeImmutable 对象。

下面的程序演示了 PHP 中的 DateTimeImmutable：：Add()函数：

**程序 1：**此程序使用 DateTimeImmutable：：Add()函数向 DateTimeImmutable 对象添加 2 天。

```
<?php
// PHP program to illustrate DateTimeImmutable::add()
// function

// Creating a new DateTimeImmutable::add() object
$datetime = new DateTimeImmutable("2019-10-03T10:00:00");

// Initializing a date interval of 2 days
$interval = 'P2D';

// Calling the add() function
$datetime = $datetime->add(new DateInterval($interval));

// Getting a new date time in the
// format of 'Y-m-d H:i:s'
echo $datetime->format('Y-m-d H:i:s');
?>
```

**输出：**

```
2019-10-05 10:00:00

```

**程序 2：**此程序使用 DateTimeImmutable：：Add()函数将‘P2Y5M2DT0H30M40S’DateInterval 添加到 DateTimeImmutable 对象。

```
<?php
// PHP program to illustrate DateTimeImmutable::add()
// function

// Creating a new DateTimeImmutable::add() object
$datetime = new DateTimeImmutable("2019-10-03T10:00:00");

// Initializing a DateInterval object
$interval = 'P2Y5M2DT0H30M40S';

// Calling the add() function
$datetime = $datetime->add(new DateInterval($interval));

// Getting a new date time in the
// format of 'Y-m-d H:i:s'
echo $datetime->format('Y-m-d H:i:s');
?>
```

**输出：**

```
2022-03-05 10:30:40

```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.add.php](https://www.php.net/manual/en/datetimeimmutable.add.php)