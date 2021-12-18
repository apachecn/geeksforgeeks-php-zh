# PHP|IntlCalendar getType()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-gettype-function/](https://www.geeksforgeeks.org/php-intlcalendar-gettype-function/)

**IntlCalendar：：getType()函数**是 PHP 中的一个内置函数，用于获取字符串形式的日历类型。 “日历”是关键字的有效值。

**语法：**

*   Object-oriented style

    ```php
    *string* IntlCalendar::getType( *void* )
    ```

*   Process style

    ```php
    *string* intlcal_get_type( *IntlCalendar* $cal )
    ```

**参数：**此函数接受单个参数**$cal**，该参数保存 IntlCalendar 的资源。

**返回值：**此函数返回表示日历类型的字符串值。

下面的程序演示了 PHP 中的 IntlCalendar：：getType()函数：

**程序：**

```php
<?php

// Set the date timezone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('intl.default_locale', 'en_US');

// Create an instance of calendar
$calendar = IntlCalendar::createInstance(NULL, 'en_US');

// Display the calendar tyle
var_dump($calendar->getType());

// Create an instance of calendar
$calendar = IntlCalendar::createInstance(NULL, '@calendar=islamic');

// Display the calendar tyle
var_dump($calendar->getType());

// Creare a DateTime object
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29'); 

// Display the calendar tyle
var_dump($calendar->getType());

?>
```

**输出：**

```php
string(9) "gregorian"
string(7) "islamic"
string(9) "gregorian"

```

**引用：**[https://www.php.net/manual/en/intlcalendar.gettype.php](https://www.php.net/manual/en/intlcalendar.gettype.php)