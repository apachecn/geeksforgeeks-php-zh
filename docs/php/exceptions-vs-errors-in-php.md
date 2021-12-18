# 异常与 PHP 中的错误

> 原文:[https://www.geeksforgeeks.org/exceptions-vs-errors-in-php/](https://www.geeksforgeeks.org/exceptions-vs-errors-in-php/)

**错误:**错误是一个意外的程序结果，程序本身无法处理。这可以通过手动使用代码中的问题来解决。错误可能是程序本身无法处理的无限循环，因此您必须手动修复该问题。有一个处理错误的简单程序，即使用**模具()**功能。
**语法:**

```php
die("message")
```

**程序:**

```php
<?php

// Open file in read mode
$file_var = fopen("myfile.txt", "r");

// Check for file existence
if (!file_exists("myfile.txt")) {
    die("Sorry Error!! file does not exists");
}
else {
    fopen("myfile.txt", "r");
}

?>
```

**输出:**

```php
Sorry Error!! file does not exists

```

**异常:**异常也是程序的意外结果，但异常可以由程序自己通过抛出另一个异常来处理。异常应该只用于错误条件，其中错误是不可删除的。使用**试**和**抓**的方法有一个克服异常的简单方法。

**语法:**

```php
try {

}
catch {

}

```

**程序:**

```php
<?php

function valid_division($x, $y) {

    if($y != 0) {
        return true;
    }
    else {
        throw new Exception("Why should not be equal to 0");
    }
}

try {
    valid_division(2, 0);

    // Try block will only run if 
    // there is no exception
    echo "Valid division";
}
catch(Exception $e) {

    // Catch block will run if an
    // exception occurs
    echo "Error\n";
    echo $e->getmessage();
}

?>
```

**输出:**

```php
Error
Why should not be equal to 0

```

**差异汇总:**

| 错误 | 例外 |
| 错误是程序方法。 | 异常是面向对象的编程方法。 |
| PHP 中默认的错误处理非常简单。带有文件名、行号和描述错误的消息的错误消息被发送到浏览器。 | 异常用于在出现指定错误时更改脚本的正常流程。 |
| 这可以使用 **PHP die()** 函数来完成。 | 使用抛出新异常()的基本异常处理在提前异常处理的情况下，您必须使用**尝试**和**捕捉**方法。 |
| 错误主要是由程序运行的环境引起的。 | 程序本身负责导致异常。 |

**注意:** PHP 默认是一种异常轻语言，但是在使用面向对象的代码时，可以将错误变成异常。