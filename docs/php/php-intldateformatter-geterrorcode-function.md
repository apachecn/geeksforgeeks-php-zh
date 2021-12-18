# PHP|IntlDateForMatter getErrorCode()函数，

> Original: [https://www.geeksforgeeks.org/php-intldateformatter-geterrorcode-function/](https://www.geeksforgeeks.org/php-intldateformatter-geterrorcode-function/)

**IntlDateForMatter：：getErrorCode()函数**是 PHP 中的内置函数，用于返回上次操作的错误代码。

**语法：**

*   Object-oriented style:

    ```
    *int* IntlDateFormatter::getErrorCode( *void* )
    ```

*   Process style:

    ```
    *int* datefmt_get_error_code( *IntlDateFormatter* $fmt )
    ```

**参数：**此函数使用单个参数**$fmt**，该参数保存格式化程序的资源。

**返回值：**此函数返回错误代码，UErrorCode 值之一。 初始值为 U_ZERO_ERROR。

下面的程序演示了 PHP 中的 IntlDateForMatter：：getErrorCode()函数：

**程序：**

```
<?php

// Create a date formatter
$formatter = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::SHORT,
    'Asia/Kolkata',
    IntlDateFormatter::GREGORIAN
);

// Format the date/time value
// as a string
$str = datefmt_format($formatter);

if (!$str) {
    echo "Error code: " . 
        datefmt_get_error_code($formatter) . "\n";

    echo "Error message: " . 
        datefmt_get_error_message($formatter);
}

echo "\n\n";

// Format the date/time value
// as a string
$str = $formatter->format("geeks");

if (!$str) {
    echo "Error code: " . 
        $formatter->getErrorCode() . "\n";

    echo "Error message: " . 
        $formatter->getErrorMessage();
}

?>
```

**错误：**

```
PHP Warning:  datefmt_format() expects exactly 2 parameters, 1 given
in /home/700d8660f05cec95beb6e1ab21252ab1.php on line 14
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/intldateformatter.geterrorcode.php](https://www.php.net/manual/en/intldateformatter.geterrorcode.php)