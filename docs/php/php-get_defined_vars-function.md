# PHP|get_fined_vars()函数

> Original: [https://www.geeksforgeeks.org/php-get_defined_vars-function/](https://www.geeksforgeeks.org/php-get_defined_vars-function/)

GET_DEFINED_vars()函数是 PHP 中的一个内置函数，用于返回所有已定义变量的数组。 此函数返回一个多维数组，其中包含变量、环境等的所有列表。

**语法：**

```
array get_defined_vars( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回所有变量的多维数组。

下面的程序演示了 PHP 中的 get_fined_vars()函数：

**程序：**

```
<?php

// Declare an array and initialize it
$a = array(0, 1, 2, 3, 4);

// Use get_defined_vars() function
$a = get_defined_vars();

// Display the output
print_r($a);
?>
```

**输出：**

```
Array
(
    [_GET] => Array
        (
        )

    [_POST] => Array
        (
        )

    [_COOKIE] => Array
        (
        )

    [_FILES] => Array
        (
        )

    [argv] => Array
        (
            [0] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
        )

    [argc] => 1
    [_SERVER] => Array
        (
            [PHP_SELF] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
            [SCRIPT_NAME] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
            [SCRIPT_FILENAME] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
            [PATH_TRANSLATED] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
            [DOCUMENT_ROOT] => 
            [REQUEST_TIME_FLOAT] => 1543316494.2727
            [REQUEST_TIME] => 1543316494
            [argv] => Array
                (
                    [0] => /home/9485b6f3bafb5e0e7b2d4580a85e639d.php
                )

            [argc] => 1
        )

    [a] => Array
        (
            [0] => 0
            [1] => 1
            [2] => 2
            [3] => 3
            [4] => 4
        )

)

```

**引用：**[http://php.net/manual/en/function.get-defined-vars.php](http://php.net/manual/en/function.get-defined-vars.php)