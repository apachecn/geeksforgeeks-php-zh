# PHP|错误类型

> Original: [https://www.geeksforgeeks.org/php-types-of-errors/](https://www.geeksforgeeks.org/php-types-of-errors/)

错误是程序中的错误或错误。 它可以是几种类型。 错误可能是由于错误的语法或错误的逻辑导致的。 这是一种错误或对代码有不正确认识的情况。

PHP 中有各种类型的错误，但它包含**基本上四种主要类型的错误**。

1.  **Parse error or Syntax Error:** It is the type of error done by the programmer in the source code of the program. The syntax error is caught by the compiler. After fixing the syntax error the compiler compile the code and execute it. Parse errors can be caused dues to unclosed quotes, missing or Extra parentheses, Unclosed braces, Missing semicolon etc
    **Example:**

    ```
    <?php
    $x = "geeks";
    y = "Computer science";
    echo $x;
    echo $y;
    ?>
    ```

    **错误：**

    ```
    PHP Parse error:  syntax error, unexpected '=' 
    in /home/18cb2875ac563160a6120819bab084c8.php on line 3

    ```

    **解释：**在上述程序中，第 3 行中缺少**$符号，因此它会给出错误信息。**

2.  **致命错误：**这是一种错误类型，PHP 编译器可以理解 PHP 代码，但它可以识别未声明的函数。 这意味着在没有定义函数的情况下调用函数。
    **示例：**

```
<?php

function add($x, $y)
{
    $sum = $x + $y;
    echo "sum = " . $sum;
}
$x = 0;
$y = 20;
add($x, $y);

diff($x, $y);
?>
```

**错误：**

```
PHP Fatal error:  Uncaught Error: 
Call to undefined function diff() 
in /home/36db1ad4634ff7deb7f7347a4ac14d3a.php:12

Stack trace:
#0 {main}
  thrown in /home/36db1ad4634ff7deb7f7347a4ac14d3a.php on line 12

```

**说明：**第 12 行调用了函数，但函数定义不可用。 所以它会产生误差。

9.  **Warning Errors :** The main reason of warning errors are including a missing file. This means that the PHP function call the missing file.
    **Example:**

    ```
    <?php 

    $x = "GeeksforGeeks";

    include ("gfg.php");

    echo $x . "Computer science portal";
    ?>
    ```

    **错误：**

    ```
    PHP Warning:  include(gfg.php): failed to 
    open stream: No such file or directory in 
    /home/aed0ed3b35fece41022f332aba5c9b45.php on line 5
    PHP Warning:  include(): Failed opening 'gfg.php'
     for inclusion (include_path='.:/usr/share/php') in 
    /home/aed0ed3b35fece41022f332aba5c9b45.php on line 5

    ```

    **解释：**此程序调用不可用的未定义文件 gfg.php。 所以它会产生错误。

10.  **Notice Error:** It is similar to warning error. It means that the program contains something wrong but it allows the execution of script.
    **Example:**

    ```
    <?php 

    $x = "GeeksforGeeks";

    echo $x;

    echo $geeks;
    ?>
    ```

    **错误：**

    ```
    PHP Notice:  Undefined variable: geeks in 
    /home/84c47fe936e1068b69fb834508d59689.php on line 5

    ```

    发帖主题：Re：Колибри0.7.0

    ```
    GeeksforGeeks

    ```

    **解释：**此程序使用**未声明变量**$geek，因此它会给出错误消息。

**PHP 错误常量及其说明：**

*   **E_ERROR：**导致脚本终止的致命错误
*   **E_WARNING：**不会导致脚本终止的运行时警告
*   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
*   **E_NOTICE：**代码错误导致的运行时通知
*   **E_CORE_ERROR：**PHP 初始启动(安装)期间发生的致命错误
*   **E_CORE_WARNING：**PHP 初始启动期间出现的警告
*   **E_COMPILE_ERROR：**脚本出现致命的编译时错误指示问题。
*   **E_USER_ERROR：**用户生成的错误消息。
*   **E_USER_WARNING：**用户生成的警告消息。
*   **E_USER_NOTICE：**用户生成的通知消息。
*   **E_Strict：**运行时通知。
*   **E_RECOVERABLE_ERROR：**可捕获的致命错误，表示存在危险错误
*   **E_Deposated：**运行时通知。