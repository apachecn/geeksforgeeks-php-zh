# PHP|DateTimeImmutable：：Sub()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutablesub-function/](https://www.geeksforgeeks.org/php-datetimeimmutablesub-function/)

DateTimeImmutable：：Sub()函数是 PHP 中的一个内置函数，用于从创建的 DateTimeImmutable 对象中减去若干天、月、年、小时、分钟和秒。

**语法：**

```php
DateTimeImmutable::sub( interval )

```

**参数：**此函数接受参数**interval**，它是要从给定的 DateTimeImmutable 对象中减去的天数、月数、年数、小时数、分钟数或秒数。

**返回值：**：此函数返回减法后的最终日期时间。

以下程序说明了 DateTimeImmutable：：Sub()函数：

**程序 1**：此程序将天数减少 2 天。

```php
<?php
// PHP program to illustrate DateTimeImmutable::sub()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable('2019-10-07');

// Initialising a interval of 2 days
$interval = 'P2D';

// Calling the DateTimeImmutable::sub() function
$a = $datetimeImmutable->sub(new DateInterval($interval));

// Getting a new date time
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

发帖主题：Re：Колибри0.7.0

```php
2019-10-05

```

**程序 2**：此程序将月份减少 5。

```php
<?php
// PHP program to illustrate DateTimeImmutable::sub()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable('2019-10-07');

// Initialising a interval of 5 months
$interval = 'P5M';

// Calling the DateTimeImmutable::sub() function
$a = $datetimeImmutable->sub(new DateInterval($interval));

// Getting a new date time
// format of 'Y-m-d'
echo $a->format('Y-m-d');
?>
```

发帖主题：Re：Колибри0.7.0

```php
2019-05-07

```

**参考**
[https://devdocs.io/php/datetimeimmutable.sub](https://devdocs.io/php/datetimeimmutable.sub)