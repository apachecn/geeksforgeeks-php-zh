# 如何在 PHP 中获取调用函数/方法的名称？

> 原文:[https://www . geesforgeks . org/how-to-name-of-calling-function-method-in-PHP/](https://www.geeksforgeeks.org/how-to-get-name-of-calling-function-method-in-php/)

为什么需要获取调用函数的名称？
代码由执行不同任务但彼此直接或间接相关联的多个函数组成，并且突然在某些函数中显示错误，则有必要找到发生错误的函数的名称。

**进场:**

*   声明一个用户定义的函数*调用函数名()*，它将作为调试器函数(它跟踪脚本中的另一个函数)。
*   使用“new”关键字创建异常类的引用。
*   现在使用这个引用变量调用内置函数 *getTrace()* (它是 Exception 类的成员函数)。
*   获取任何变量中 getTrace()函数返回的值(getTrace()函数返回关联数组)。
*   使用 print_r()函数打印该变量。
*   创建一个或多个用户定义的函数来测试跟踪函数。

**例 1:**

```
<?php
// PHP program to get the name
// of calling function/method

function CallingFunctionName() {

    // Create an exception
    $ex = new Exception();

    // Call getTrace() function
    $trace = $ex->getTrace();

    // Position 0 would be the line
    // that called this function
    $final_call = $trace[1];

    // Display associative array 
    print_r($final_call);
}

// Declare firstCall() function
function firstCall($x, $y) {

    // Call secondCall() function
    secondCall($x, $y);
}

// Declare secondCall() function
function secondCall($x, $y) {

    // Call CallingFunctionName()
    // function
    CallingFunctionName();
}

// Call firstCall() function
firstCall('test', 'php');

?>
```

**Output:**

```
Array
(
    [file] => /home/5aeb55f2023e4e59fedcedc30e37e060.php
    [line] => 26
    [function] => secondCall
    [args] => Array
        (
            [0] => test
            [1] => php
        )

)

```

**解释:***getTrace()*函数将扫描整个方法调用堆栈，并以关联数组的形式存储所有信息。关联数组包含以下信息。

*   **【文件】:**当前 PHP 文件的绝对路径。
*   **【行】:**已调用函数‘CallingFunctionName()’的行号。
*   **【函数】:**携带调用函数的名称。
*   **[args]:** 给出调用函数的参数值。

在第 15 行，将值 1 作为 trace[]的下标传递，这样它会返回堆栈中最上面的函数的所有信息。

**例 2:**

```
<?php
// PHP program to get the name
// of calling function/method

function CallingFunctionName() {

    // Create an exception
    $ex = new Exception();

    // Call getTrace() function
    $trace = $ex->getTrace();

    // Position 0 would be the line
    // that called this function
    $final_call = $trace[2];

    // Display associative array 
    print_r($final_call);
}

// Declare firstCall() function
function firstCall($x, $y) {

    // Call secondCall() function
    secondCall($x, $y);
}

// Declare secondCall() function
function secondCall($x, $y) {

    // Call CallingFunctionName()
    // function
    CallingFunctionName();
}

// Call firstCall() function
firstCall('test', 'php');

?>
```

**Output:**

```
Array
(
    [file] => /home/1b5518d5af0615813238e7534ccb6e8a.php
    [line] => 38
    [function] => firstCall
    [args] => Array
        (
            [0] => test
            [1] => php
        )

)

```

**说明**:输出包含函数 *firstcall()* 的所有信息，因为下标 trace 的值是 2。

*   **轨迹[0]:** 位置 0 将是函数本身(这里称为函数名())。
*   **trace[1]:** 位置 1 将是函数*秒调用*，因为这是调用堆栈中最上面的函数。
*   **跟踪[2]:** 位置 2 将是函数“第一次调用”，因为这是调用堆栈中的前 1 个函数。
*   **trace[n]:** 位置 n 将是第 n 个函数，因为这是调用堆栈中最上面的第 n 个函数。