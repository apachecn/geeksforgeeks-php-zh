# PHP 中 try-catch 和 if-else 语句的区别

> 原文:[https://www . geeksforgeeks . org/try-catch-and-if-else-statements-in-PHP/](https://www.geeksforgeeks.org/difference-between-try-catch-and-if-else-statements-in-php/)

PHP 中使用 **try** 和 **catch** 来处理异常，就像 C++、Java 等其他语言一样。异常是程序本身可以处理的意外结果或意外状态。在 PHP 中处理这种意想不到的结果，使用**尝试**和**捕捉**。更多详细信息，请访问 PHP 中的[异常处理](https://www.geeksforgeeks.org/exception-handling-in-php/)。

同样，PHP 也使用**和 **else** 执行条件语句来处理决策场景。更多详情，请访问 [PHP |决策](https://www.geeksforgeeks.org/php-decision-making/)**

****PHP 中“try-catch”和“if-else”的区别:****

****什么是*****【if】*****和*****【else】*****？****

*   ****如果:**它检查任何条件是否为“真”，如果为真，则它执行 *if* 块内的代码。**
*   ****否则:**如果条件为“假”，则由 *if* 块检查，然后 *else* 块执行其中的其他代码。**

```
if(condition)
{......}
else
{......} 
```

**或者**

```
if(condition)
{......}
else if(condition)
{......}
else
{......}
```

****什么是******和** ***【赶】*** **？******

*   ******try:** 这是一个定义代码块的部分，用于测试代码在执行时是否产生意外结果。****
*   ******catch:** 它是定义另一个代码块的部分，如果在 try 块中产生任何意外结果，就会执行该代码块。实际上，这段代码处理异常。**** 

```
**try
{...condition...;
 ...condition..;
 .....;
 .....;
 .....;
}
catch (Exception)
{...handling exception...;}**
```

******错误处理:**主要是 **if-else** 块用于使用条件检查处理错误。 **if-else** 捕捉错误作为条件语句。在许多情况下，在执行过程中有许多必须检查的情况，但是“如果-否则”只能处理定义的条件。在 **if-else** 中，基于任务手动生成条件。****

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
**<?php

$g = "GeeksforGeeks";

// Checks for a condition if
// 'g'is null or not
if ($g != "") {
    echo $g;
}

else {
    echo "This is not the string";
}
?>**
```

******输出:******

```
**GeeksforGeeks**
```

****在**试捕**块的情况下，它将检查系统在执行过程或任务中产生的错误或异常。这些错误或异常不是手动生成的。**试捕**处理容易阅读的异常。****

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
**<?php

// Exception handling function
function tryCatchException($b, $var) {

    try {
        echo "\nDivision is ", $b/$var;
        throw new Exception('denominator is 0');
        // If 'var' is zero then exception
        // is thrown
    }
    // Catch block will be executed if
    // any Exception has been thrown
    // by try block
    catch(Exception $e)    {
        echo "\nException: ", $e->getMessage();
        // Print the Message passed
        // by the thrown statement
    }
}

// Exception will happened
tryCatchException(6, 0);

?>**
```

******输出:****** 

```
**Runtime Errors : 
PHP Warning:  Division by zero in 
/home/1027ff9c161eb6503f545005908318fc.php on line 8
Division is INF
Exception: denominator is 0** 
```

******用一个块处理错误或异常:**如果是 **if-else** 我们有一个 **else** 块对应一个 **if** 块，所以我们要用一个 **else** 块定义每个 **if** 块来处理“假”情况。如果，在**之后可能没有任何**或者**的语句。******

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

function rngeLaptop($a) {

    // Each 'if' with one 'else'
    if ($a == "Gaming") {
        echo "Range stated from 50000rs\n";
    }

    else if($a == "Education") {
        echo "Range stated from 25000rs\n";
    }

    else if($a == "Graphics works") {
        echo "Range stated from 55000rs\n";
    }

    else if($a == "Entertainment") {
        echo "Range stated from 18000rs\n";
    }
    else {
        echo "Not listed\n";
    }
}

rngeLaptop("Gaming");
rngeLaptop("Education");
rngeLaptop("Movie"); // Not listed
rngeLaptop("Entertainment");
rngeLaptop("Graphics works");

?>
```

****输出:****

```
Range stated from 50000rs
Range stated from 25000rs
Not listed
Range stated from 18000rs
Range stated from 55000rs
```

**在**试捕**的情况下，我们不必用**抓**来定义每个**试捕**。一个 **try** 里面可以定义多个异常，要捕捉 **try** 块抛出的异常，可以有一个 **catch** 块。**

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

// Exception handling function
function tryCatchException($b, $var) {
    try {

        // Checking 2 condition and throwing
        // all exceptions in one catch block
        if($var == 0) {
            throw new Exception('denominator is 0');
        }
        if($var < 0) {
            throw new Exception('denominator is a negative');
        }
        echo "\nDivision is ", $b/$var;
    }

    // Catch block will be executed if any
    // Exception has been thrown by try block
    catch(Exception $e) {

        // Print the Message passed by
        // the thrown statement  
        echo "\nException: ", $e->getMessage();
    }
}

// Exception will happened
tryCatchException(6, -3);
tryCatchException(12, 0);
tryCatchException(15, 3);

?>
```

****输出:****

```
Exception: denominator is a string
Exception: denominator is 0
Division is 5 
```

****PHP 中“try-catch”和“if-else”的区别简述:****

<figure class="table">

| 如果-否则 | 试捕 |
| It checks whether any condition is true, if it is true, it executes the code inside the IF block, otherwise, it executes the else block. | "try" is the part that defines the code, which is used to test whether the code produces unexpected results when it is executed. If any unexpected results are found, the catch block is executed to deal with this situation. |
| [if-else] Use condition check to deal with different conditions. | In the case of "trial capture", the system will check the errors or exceptions generated by the system during execution or tasks. |
| Conditions are generated manually in' if-else'. According to the task. | Try-catch handles errors generated by the system, such as array out of bounds, division by zero, etc. |
| In "if-else", the conditions are mixed with the code in the block, so if there are many "if-else" blocks, it becomes unreadable. | In "try-catch", the code for handling exceptions and what exceptions to handle are easy to read. |
| In' if-else', we have an else block corresponding to an if block. Or we need to define another condition with the command "else if". | In' try-catch', we don't have to use' catch' blocks to define each' try' block. |
| "if-else" takes less time than "try-catch". | "Try catching" is more time-consuming than "if-else". |
| [if-else] Communicate between data and conditions provided to the program. | [Trial capture] Communicate between conditional data and systems. |

</figure>