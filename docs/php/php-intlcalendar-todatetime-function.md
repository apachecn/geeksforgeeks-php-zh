# PHP|IntlCalendar toDateTime()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-todatetime-function/](https://www.geeksforgeeks.org/php-intlcalendar-todatetime-function/)

**IntlCalendar：：toDateTime()函数**是 PHP 的内置函数，用于将 IntlCalendar 对象转换为 DateTime 对象。 DateTime 对象表示精度高达秒，四舍五入误差小于 1 秒。

**语法：**

*   Object-oriented style

    ```php
    *DateTime* IntlCalendar::toDateTime( *void* )
    ```

*   Process style

    ```php
    *DateTime* intlcal_to_date_time( *IntlCalendar* $cal )
    ```

**参数：**此函数接受单个参数**$cal**，该参数保存 IntlCalendar 对象的资源。

**返回值：**此函数返回一个 DateTime 对象，该对象与此对象具有相同的时区和相同的时间，只是成功时的精度较小，失败时返回 False。

下面的程序演示了 PHP 中的 IntlCalendar：：toDateTime()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('date.timezone', 'UTC');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Convert the IntlCalendar into a DateTime object
$datetime = $calendar->toDateTime();

// Display the DateTime object
var_dump($datetime);

// Declare a IntlGregorianCalendar
$calendar = new IntlGregorianCalendar(2019, 9, 22, 12, 40, 0);

// Convert the IntlGregorianCalendar into
// a DateTime object
$datetime = $calendar->toDateTime();

// Display the DateTime object
var_dump($datetime);

?>
```

**输出：**

```php
object(DateTime)#3 (3) {
  ["date"]=>
  string(26) "2019-09-25 11:15:33.000000"
  ["timezone_type"]=>
  int(3)
  ["timezone"]=>
  string(13) "Asia/Calcutta"
}
object(DateTime)#4 (3) {
  ["date"]=>
  string(26) "2019-10-22 12:40:00.000000"
  ["timezone_type"]=>
  int(3)
  ["timezone"]=>
  string(3) "UTC"
}

```

**引用：**[https://www.php.net/manual/en/intlcalendar.todatetime.php](https://www.php.net/manual/en/intlcalendar.todatetime.php)