# PHP|date_create()、date_format()、date_add()函数

> Original: [https://www.geeksforgeeks.org/php-date_create-date_format-date_add-functions/](https://www.geeksforgeeks.org/php-date_create-date_format-date_add-functions/)

在某个时间点，我们需要在日期和时间中添加一些天、月、年、小时、分钟和秒。 PHP 为我们提供了几个执行此操作的内置函数。 我们将在这里讨论的一些内置函数包括 date_create()、date_format()和 date_add()。

**date_create()函数**

此函数用于使用日期/时间字符串和时区创建 DateTime 对象。 日期/时间字符串的默认值为当前日期/时间。
**语法：**

```php
*DateTime* date_create(time, timezone);

```

**参数：**此函数接受两个参数：

1.  **时间：**(可选)指定日期/时间字符串。 NULL 或默认值
    表示当前日期/时间。 您可以参考[此链接](http://php.net/manual/en/datetime.formats.php)了解 PHP 中支持的日期和时间格式。
2.  **时区：时间的**(可选)时区。

**返回值**：此函数返回指定日期的新 DateTime 对象。

**date_format()函数**

函数的作用是：设置给定日期的格式。 日期作为 DateTime 实例提供，该实例通常由 date_create()函数返回，Format 是我们要根据其格式化日期的字符串。

**语法：**

```php
*string* date_format(object, format);

```

**参数：**此函数接受两个参数，这两个参数都是必须提供的。

1.  **对象：**指定由 date_create()返回的 DateTime 对象
2.  **格式：**指定日期的格式。 它接受 PHP 中 date()函数支持的格式。 示例-H(24 小时格式)、h(12 小时格式)、i(分钟：00 到 59)、s(秒：00 到 59)等。

**返回值**：date_format()函数返回一个字符串，该字符串表示成功格式化时按照指定格式格式化的日期，否则在失败时返回 False。

```php
<?php

// using date_create() function to create
// DateTime object
$date=date_create("2018-03-15");

// using date_format() function to format date
echo date_format($date, "Y/m/d H:i:s");

?>
```

产出：

```php
2018/03/15 00:00:00

```

**date_add()函数**

函数的作用是：向日期添加日、月、年、小时、分钟和秒。 日期作为 DateTime 对象提供给 date_add()函数，我们想要添加到 Date 中的时间间隔作为 DateInterval 对象提供。

**语法：**

```php
*DateTime* date_add(object, interval);

```

**参数：**此函数接受三个参数，所有这些参数都是必须提供的。

1.  **对象：**指定由 date_create()返回的 DateTime 对象。 此函数返回一个新的 DateTime 对象。
2.  **Interval：**指定 DateInterval 对象，即它以 DateTime 的构造函数支持的格式存储固定的时间量(以年、月、日、小时等表示)或相对时间字符串。

**返回值：**此函数成功时返回 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 date_add()函数：

**示例-1**

```php
<?php

// PHP program to add 40 days in date

$date=date_create("2018-12-10");

date_add($date, date_interval_create_from_date_string("40 days"));

echo date_format($date, "Y-m-d");

?>
```

产出：

```php
2019-01-19

```

**示例-2**

```php
<?php

//PHP program to add 1 year, 10 mins, 23 secs in date

$date=date_create("2018-12-10");

date_add($date, date_interval_create_from_date_string("1 year 
                                      + 10 mins + 23 secs"));

echo date_format($date, "Y-m-d H:i:s");

?>
```

产出：

```php
2019-12-10 00:10:23

```

**注意**：使用‘+’运算符可以向日期和时间添加更多内容。

发帖主题：Re：Колибри0.7.0

*   [http：//php.net/manual/en/datetime.format.php](http://php.net/manual/en/datetime.format.php)
*   [http：//php.net/manual/en/function.date-add.php](http://php.net/manual/en/function.date-add.php)
*   [http：//php.net/manual/en/datetime.construct.php](http://php.net/manual/en/datetime.construct.php)