# PHP|IntlCalendar getErrorCode()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-geterrorcode-function/](https://www.geeksforgeeks.org/php-intlcalendar-geterrorcode-function/)

**IntlCalendar：：getErrorCode()函数**是 PHP 中的一个内置函数，它返回对此对象的最后一次调用的数字 ICU 错误代码或为日历参数给定的 IntlCalendar。 此功能可指示警告消息(负错误代码)或无错误。

**语法：**

*   Object-oriented style

    ```php
    *int* IntlCalendar::getErrorCode( *void* )
    ```

*   Process style

    ```php
    *int* intlcal_get_error_code( *IntlCalendar* $calendar )
    ```

**参数：**此函数使用单个参数**$caleal**，该参数保存过程化样式界面上的日历对象。

**返回值：**此函数返回 ICU 错误代码，指示成功、失败或警告消息。

下面的程序演示了 PHP 中的 IntlCalendar：：getErrorCode()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Set the intl error level
ini_set("intl.error_level", E_WARNING);

// Declare a DateTime object and store it into variable
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

// Display the error code and message
var_dump(
    $calendar->getErrorCode(),
    $calendar->getErrorMessage()
);

// Declare a DateTime object and store it into variable
$calendar->fieldDifference(-34E403, IntlCalendar::FIELD_ZONE_OFFSET);

// Display the error code and message
var_dump(
    $calendar->getErrorCode(),
    $calendar->getErrorMessage()
);

?>
```

**输出：**

```php
PHP Warning:  IntlCalendar::fieldDifference(): intlcal_field_difference: Call to ICU method has
failed in /home/d0608573e6cb44f285316ff59fb833b0.php on line 19
int(0)
string(12) "U_ZERO_ERROR"
int(1)
string(81) "intlcal_field_difference: Call to ICU method has failed: U_ILLEGAL_ARGUMENT_ERROR"

```

**引用：**[https://www.php.net/manual/en/intlcalendar.geterrorcode.php](https://www.php.net/manual/en/intlcalendar.geterrorcode.php)