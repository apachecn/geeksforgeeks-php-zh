# PHP DEBUG_Backtrace()函数

> Original: [https://www.geeksforgeeks.org/php-debug_backtrace-function/](https://www.geeksforgeeks.org/php-debug_backtrace-function/)

**DEBUG_Backtrace()函数**是 PHP 中的一个内置函数，程序员通常在调试时使用该函数。 Debug_backtrace()函数的主要工作是生成 PHP 回溯，即检查堆栈跟踪。 它返回一个由回溯 PHP 代码的关联数组组成的数组。 此函数返回的所有可能元素为-

<figure class="table">。 ]调用 DEBUG_Backtrace()函数的函数的名称。

| ***Name*** | ***Type*** | ***Description*** |
| 功能 / 目的 / 函数关系 | 细绳 |
| 线 / 绳 / 行 / 排 | Integer number | The current line number of the function call. |
| 文件夹 / 卷宗 / 文件 / 锉刀 | 细绳 | The name of the file that has called the DEBUG_Backtrace () function. |
| 等级 / 种类 / 社会等级 / 班级 | String | The name of the class that has called the DEBUG_Backtrace () function. |
| 东西 / 对象 / 目标 / 物体 | 东西 / 对象 / 目标 / 物体 | The name of the object used to call the member function in which the DEBUG_Backtrace () function exists. |
| 类型 / 品种 / 象征 / 印刷文字 | 细绳 | The type of the current call. Returns "- >" if the current call type is a method call. If it is a static method call, it returns "::" and if it is a function call, nothing is returned. |
| ARGS | 有序的安排 / 排列 / 大批 | A list of parameters that exist in the function definition. If you use the DEBUG_Backtrace () function in a file, all files contained in that file are returned. For example, |

</figure>

**语法：**

```php
*array* debug_backtrace(*int* $options, *int* $limit);
```

这里，参数**$Options**和**$Limit**都是可选的，并且都是整型的。 **$OPTION**参数用于位掩码，**$Limit**可用于设置要打印的堆栈帧数量限制。 $Limit 的默认值设置为零。

示例：在此示例中，我们创建了一个返回两个输入参数之和的函数，并在该函数中使用了 DEBUG_Backtrace()函数。 在打印输出时，首先显示输入参数的总和，然后打印代码的回溯。

## PHP

```php
<?php

function sum($a, $b) {
    echo $a + $b . "\n\n";

    var_dump(debug_backtrace());
}

sum(10,2);

?>
```

**OUTPUT**

```php
12

array(1) {
  [0]=>
  array(4) {
    ["file"]=>
    string(42) "/home/2228b7c9e401174a5f773007cd840e32.php"
    ["line"]=>
    int(9)
    ["function"]=>
    string(3) "sum"
    ["args"]=>
    array(2) {
      [0]=>
      int(10)
      [1]=>
      int(2)
    }
  }
}
```