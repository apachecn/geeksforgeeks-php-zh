# PHP|DateTimeImmutable Modify()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-modify-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-modify-function/)

**DateTimeImmutable：：Modify()函数**是 PHP 中的内置函数，用于修改或更改创建的 DateTimeImmutable 对象的时间戳。

**语法：**

```php
*DateTimeImmutable* DateTimeImmutable::modify( *string* $modify )

```

**参数：**此函数使用上述两个参数，如下所述：

*   **object:** this parameter holds the DateTime object returned by the date_create () function.
*   **$Modify** this parameter holds a date / time string that sets the time to change a given DataTimeImmutable object.

**返回值：**此函数成功时返回修改后的 DateTimeImmutable 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DateTimeImmutable：：Modify()函数：

**程序 1：**本程序修改给定日期，增量为 5 天。

```php
<?php
// PHP program to illustrate DateTimeImmutable::modify()
// function

// creating a DateTime object
$datetimeImmutable = new DateTimeImmutable('2019-10-02T00:00:00');

// Calling of date DateTimeImmutable::modify() function
// with the increment of 5 days as parameters
$newDateTimeImmutable = $datetimeImmutable->modify('+5 days');

// Getting the modified date in "y-m-d" format
echo $newDateTimeImmutable->format('Y-m-d');
?>
```

**输出：**

```php
2019-10-07

```

**程序 2：**本程序修改给定日期，增量为 2 个月。

```php
<?php
// PHP program to illustrate DateTimeImmutable::modify()
// function

// Creating a DateTime object
$datetimeImmutable = new DateTimeImmutable('2019-10-02T00:00:00');

// Calling of date DateTimeImmutable::modify() function
// with the increment of 2 months as parameters
$newDateTimeImmutable = $datetimeImmutable->modify('+2 months');

// Getting the modified date in "y-m-d" format
echo $newDateTimeImmutable->format('Y-m-d');
?>
```

**输出：**

```php
2019-12-02

```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.modify.php](https://www.php.net/manual/en/datetimeimmutable.modify.php)