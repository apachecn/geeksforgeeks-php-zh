# PHP|DateTimeImmutable setTime()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-settime-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-settime-function/)

**DateTimeImmutable：：setTime()函数**是 PHP 中的一个内置函数，用于通过重置创建的 DateTimeImmutable 对象的当前时间来设置所需的时间。
**语法：**和

```php
*DateTimeImmutable* DateTimeImmutable::setTime( *int* $hour, *int* $minute,
                                              *int* $second, *int* $microseconds )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$hr：**此参数用于设置小时时间。
*   **$min：**该参数用于设置分钟时间。
*   **$Second：**此参数用于第二次设置。
*   **$microsec：**此参数用于设置微秒时间。

**返回值：**此函数返回新的 Date Time 对象。
以下程序说明 PHP：
**程序 1：**和
中的 DateTimeImmutable：：setTime()函数

## PHP

```php
<?php

// PHP program to illustrate DateTimeImmutable::setTime()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable('2019-10-04');

// Initialising Hour, Minute and Second
$Hour = '04';
$Minute = '10';
$Second = '40';

// Calling the DateTimeImmutable::setTime() function
$a = $datetimeImmutable->setTime($Hour, $Minute, $Second);

// Getting a new set of date and time in the
// format of 'Y-m-d H:i:s'
echo $a->format('Y-m-d H:i:s');
?>
```

**Output:** 

```php
2019-10-04 04:10:40
```

**程序 2：**和

## PHP

```php
<?php

// PHP program to illustrate DateTimeImmutable::setTime()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable('2019-10-04');

// Calling the setTime() function
// with parameters like Hour of 10,
// minute of 33 and second of 39
$a = $datetimeImmutable->setTime(10, 33, 39);

// Getting a new set of date and time in the
// format of 'Y-m-d H:i:s'
echo $a->format('Y-m-d H:i:s');
?>
```

**Output:** 

```php
2019-10-04 10:33:39
```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.settime.php](https://www.php.net/manual/en/datetimeimmutable.settime.php)