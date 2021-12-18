# PHP|DATE_GET_LAST_ERROR()函数

> Original: [https://www.geeksforgeeks.org/php-date_get_last_errors-function/](https://www.geeksforgeeks.org/php-date_get_last_errors-function/)

DATE_GET_LAST_ERROR()函数是 PHP 中的一个内置函数，用于返回警告和错误。 此函数解析日期/时间字符串，并返回警告和错误数组。

**语法：**

*   **process style:**

    ```
    array date_get_last_errors( void )
    ```

*   **object-oriented style:**

    ```
    array DateTime::getLastErrors( void )
    ```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含警告和错误信息的数组。

下面的程序说明了 PHP 中的 date_get_last_error()函数：

**程序 1：**

```
<?php
$date = date_create();
print_r(date_get_last_errors());
?>
```

**输出：**

```
Array
(
    [warning_count] => 0
    [warnings] => Array
        (
        )

    [error_count] => 0
    [errors] => Array
        (
        )

)

```

**程序 2：**

```
<?php
try {
    $date = new DateTime('vgdgh');
} 
catch (Exception $e) {

    // For demonstration purposes only...
    print_r(DateTime::getLastErrors());
}
?>
```

**输出：**

```
Array
(
    [warning_count] => 0
    [warnings] => Array
        (
        )

    [error_count] => 1
    [errors] => Array
        (
            [0] => The timezone could not be found in the database
        )

)

```

**相关文章：**

*   [php|gmstrftime()函数](https://www.geeksforgeeks.org/php-gmstrftime-function/)
*   [php|gettimeofday()函数](https://www.geeksforgeeks.org/php-gettimeofday-function/)
*   [php|strpTime()函数](https://www.geeksforgeeks.org/php-strptime-function/)

**引用：**[http://php.net/manual/en/datetime.getlasterrors.php](http://php.net/manual/en/datetime.getlasterrors.php)