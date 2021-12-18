# PHP|TIMEZONE_TRANSIONS_GET()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_transitions_get-function/](https://www.geeksforgeeks.org/php-timezone_transitions_get-function/)

函数的作用是：在 PHP 中内置函数，用于返回时区的所有转换。 此函数在成功时返回包含所有转换的关联数组，如果失败则返回 False。

**语法：**

*   **process style:**

    ```php
    timezone_transitions_get( $object, $timestamp_begin, $timestamp_end )
    ```

*   **object-oriented style:**

    ```php
    DateTimeZone::getTransitions( $timestamp_begin, $timestamp_end )
    ```

**参数：**此函数接受上述三个参数，如下所述：

*   **$object:** this is a mandatory parameter that specifies the DateTime object returned by the date_create () function.
*   **$TIMESTAMP_BEGIN:** this parameter is used to set BEGIN TIMESTAMP.
*   **$TIMESTAMP_END:** sets the end timestamp.

**返回值：**此函数返回包含关联数组的数组，成功时返回所有转换，失败时返回 False。

下面的程序演示了 PHP 中的 timezone_Transition_get()函数：

**程序 1：**

```php
<?php

// Set time_zone object
$time_zone = timezone_open('Asia/Kolkata');

// Set the transition of time_zone
$transition = timezone_transitions_get( $time_zone );

// Display an array containing associative
// array of all transition
print_r(array_slice($transition, 0, 3));
?>
```

**输出：**

```php
Array
(
    [0] => Array
        (
            [ts] => -9223372036854775808
            [time] => -292277022657-01-27T08:29:52+0000
            [offset] => 21200
            [isdst] => 
            [abbr] => HMT
        )

    [1] => Array
        (
            [ts] => -2147483648
            [time] => 1901-12-13T20:45:52+0000
            [offset] => 19270
            [isdst] => 
            [abbr] => MMT
        )

    [2] => Array
        (
            [ts] => -2019705670
            [time] => 1905-12-31T18:38:50+0000
            [offset] => 19800
            [isdst] => 
            [abbr] => IST
        )

)

```

**程序 2：**

```php
<?php

// Set time_zone object
$timezone = new DateTimeZone("Asia/Kolkata");

// Set the transition of time_zone
$transition = $timezone->getTransitions();

// Display an array containing associative
// array of all transition
print_r(array_slice($transition, 0, 3));
?>
```

**输出：**

```php
Array
(
    [0] => Array
        (
            [ts] => -9223372036854775808
            [time] => -292277022657-01-27T08:29:52+0000
            [offset] => 21200
            [isdst] => 
            [abbr] => HMT
        )

    [1] => Array
        (
            [ts] => -2147483648
            [time] => 1901-12-13T20:45:52+0000
            [offset] => 19270
            [isdst] => 
            [abbr] => MMT
        )

    [2] => Array
        (
            [ts] => -2019705670
            [time] => 1905-12-31T18:38:50+0000
            [offset] => 19800
            [isdst] => 
            [abbr] => IST
        )

)

```

**相关文章：**

*   [PHP|TIMEZONE_OFFSET_GET()11-13](https://www.geeksforgeeks.org/php-timezone_offset_get-function/)
*   [PHP|TIMEZONE_NAME_GET()11-13](https://www.geeksforgeeks.org/php-timezone_name_get-function/)

**引用：**[http://php.net/manual/en/datetimezone.gettransitions.php](http://php.net/manual/en/datetimezone.gettransitions.php)