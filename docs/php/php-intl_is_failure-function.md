# PHP|intl_is_ailure()函数

> Original: [https://www.geeksforgeeks.org/php-intl_is_failure-function/](https://www.geeksforgeeks.org/php-intl_is_failure-function/)

**intl_is_ailure()函数**是 PHP 中的一个内置函数，用于检查给定的错误代码是否指示失败。

**语法：**

```
*bool* intl_is_failure( $error_code )
```

**参数：**此函数接受单个参数**$error_code**，该参数是函数 intl_get_error_code()、COLLATOR_GET_ERROR_CODE()返回的值。

**返回值：**如果代码指示失败，则返回 True，如果成功或出现警告，则返回 False。

下面的程序演示了 PHP 中的 intl_is_ailure()函数：

**程序 1：**

```
<?php

// Function definition
function check( $err_code ) {
    var_export( intl_is_failure( $err_code ) );
    echo "\n";
}

// Function call using error_code as parameter
check( U_USING_FALLBACK_WARNING );
check( U_ILLEGAL_ARGUMENT_ERROR );

?>
```

**输出：**

```
false
true

```

**程序 2：**

```
<?php

// Function definition
function check( $err_code ) {
    var_export( intl_is_failure( $err_code ) );
    echo "\n";
}

// Declare an array which contains error_code
$arr = array( 
    U_ZERO_ERROR, 
    U_ILLEGAL_ARGUMENT_ERROR,
    U_USING_FALLBACK_WARNING,
);

// Loop to call function
foreach ($arr as $err) { 

    // Check each element as
    // code point data 
    check($err); 
} 

?>
```

**输出：**

```
false
true
false

```

**引用：**[https://www.php.net/manual/en/function.intl-is-failure.php](https://www.php.net/manual/en/function.intl-is-failure.php)