# PHP | call_user_func()函数

> 原文:[https://www.geeksforgeeks.org/php-call_user_func-function/](https://www.geeksforgeeks.org/php-call_user_func-function/)

call_user_func()是 PHP 中的一个内置函数，用于调用第一个参数给出的回调，并将其余参数作为参数传递。它用于调用用户定义的函数。

**语法:**

```
mixed call_user_func ( $function_name[, mixed $value1[, mixed $... ]])
```

这里，mixed 表示一个参数可以接受多种类型。
**参数:**call _ user _ func()函数接受两种类型的参数，如上所述，如下所述:

*   **$function_name:** 是已定义函数列表中函数调用的名称。它是一个字符串类型的参数。
*   **$值:**为混合值。要传递给函数的一个或多个参数。

**返回值:**该函数返回回调函数返回的值。

下面的程序说明了 PHP 中的 call_user_func()函数:

**程序 1:** 调用函数

```
<?php
function GFG($value)
{
    echo "This is $value site.\n";
}

call_user_func('GFG', "GeeksforGeeks");
call_user_func('GFG', "Content");

?>
```

**Output:**

```
This is GeeksforGeeks site.
This is Content site.

```

**程序 2:** 使用名称空间名称调用 _user_func()

```
<?php

namespace Geeks;

class GFG {
    static public function demo() {
        print "GeeksForGeeks\n";
    }
}

call_user_func(__NAMESPACE__ .'\GFG::demo'); 

// Another way of declaration
call_user_func(array(__NAMESPACE__ .'\GFG', 'demo')); 

?>
```

**Output:**

```
GeeksForGeeks
GeeksForGeeks

```

**程序 3:** 使用带有 call_user_func()的类方法

```
<?php

class GFG {
    static function show()
    {
        echo "Geeks\n";
    }
}

$classname = "GFG";
call_user_func($classname .'::show');

// Another way to use object
$obj = new GFG();
call_user_func(array($obj, 'show'));

?>
```

**Output:**

```
Geeks
Geeks

```

**程序 4:** 使用带有 call_user_func()的 lambda 函数

```
<?php
call_user_func(function($arg) { print "$arg\n"; }, 'GeeksforGeeks');
?>
```

**Output:**

```
GeeksforGeeks

```

**参考文献:**T2】http://php.net/manual/en/function.call-user-func.php