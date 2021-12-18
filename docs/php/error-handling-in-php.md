# PHP 中的错误处理

> 原文:[https://www.geeksforgeeks.org/error-handling-in-php/](https://www.geeksforgeeks.org/error-handling-in-php/)

**先决条件:** [错误类型](https://www.geeksforgeeks.org/php-types-of-errors)
PHP 用于网页开发。PHP 中的错误处理几乎类似于所有编程语言中的错误处理。PHP 中默认的错误处理会给出文件名行号和错误类型。

**处理 PHP 错误的方法:**

*   使用 die()方法
*   自定义错误处理

**基本错误处理:使用 die()函数**die()函数打印一条消息并退出当前脚本。
**语法:**

```php
die( $message )
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Php code showing default error handling

$file = fopen("geeks.txt", "w");
?>
```

**注意:**运行上面的代码并且 *geeks.txt* 文件不存在，那么它将显示一个运行时错误消息。
**运行时错误:**

```php
 PHP Warning: fopen(geeks.txt): failed to open stream: Permission denied 
in /home/dac923dff0a2558b37ba742613273073.php on line 2
```

要防止此错误，请使用 die()函数。下面是 die()函数的实现:
**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP code to check errors

// If file is not present
// then exit from script
if( !file_exists("geeks.txt") ) {
    die("File is not present");
}

// If file is present
// then continue
else {
    $file = fopen("geeks.txt", "w");
}
?>
```

**注意:**如果 *geeks.txt* 文件不存在，那么它将显示输出。
**输出**

```php
File is not present
```

**自定义错误处理:**在 PHP 中创建自定义错误处理程序非常简单。创建一个函数，当 PHP 中出现错误时可以调用它。
**语法:**

```php
error_function( $error_level, $error_message, $error_file, $error_line, $error_context)
```

**参数:**该功能接受五个参数，如上所述，描述如下:

*   **$error_level:** 必输参数，必须为整数。有预定义的错误级别。
*   **$error_message:** 必输参数，是用户要打印的消息。
*   **$error_file:** 可选参数，用于指定发生错误的文件。
*   **$error_line:** 为可选参数，用于指定发生错误的行号。
*   **$error_context:** 它是可选参数，用于在发生错误时指定包含每个变量及其值的数组。

**误差等级:**以下列出了可能的误差等级:

*   1 : .E_ERROR:脚本的致命运行时错误执行已暂停
*   2 : E_WARNING:脚本的非致命运行时错误执行已暂停
*   4 : E_PARSE:编译时错误它是由解析器生成的
*   8 :E_NOTICE:脚本发现了一些可能是错误的东西
*   16 :E_CORE_ERROR:脚本初始启动期间发生的致命错误
*   32 :E_CORE_WARNING:脚本初始启动期间发生的非致命错误
*   8191 :E_ALL:所有错误和警告

**set_error_handler()函数:**创建 myerror()函数后，需要设置自定义错误处理程序，因为在正常情况下，PHP 会处理它，但是如果用户进行自定义错误处理，那么用户必须将其设置为代替参数，并将 myerror 函数作为字符串传递出去。
T3】例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Creates my error function which prints message
//to user
function myerror($error_no, $error_msg) {
    echo "Error: [$error_no] $error_msg ";
    echo "\n Now Script will end";

    // When error occurred script has to be stopped
    die();
}

// Setting set_error_handler
set_error_handler("myerror");

$a = 10;
$b = 0;

// This will generate error
echo($a / $b);;
?>
```

**输出:**

```php
Error: [2] Division by zero 
 Now Script will end
```

**结论:**总是尝试使用自定义错误处理进行错误处理，因为它会根据用户显示更多指定的消息，可以对用户有所帮助。如果没有使用自定义错误处理来处理错误，则发生了错误，然后默认情况下将暂停输出脚本，但是如果它使用自定义错误处理来处理错误，则它可以在显示错误消息后继续脚本。