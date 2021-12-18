# PHP|ReflectionFunction Invoke()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionfunction-invoke-function/](https://www.geeksforgeeks.org/php-reflectionfunction-invoke-function/)

**ReflectionFunction：：Invoke()函数**是 PHP 中的一个内置函数，用于返回调用的函数调用的结果。

**语法：**

```
*mixed* ReflectionFunction::invoke( *mixed* $args)
```

**参数：**此函数接受参数**$args**，该参数保存传递给被调用函数的参数列表。

**返回值：**此函数返回调用的函数调用的结果。

下面的程序演示了 PHP 中的 ReflectionFunction：：Invoke()函数：

**程序 _1：**

```
<?php

// Initializing a user-defined function
function Company($Company_Name, $Role) {
    return sprintf("%s %s\r\n", $Company_Name, $Role);
}

// Using ReflectionFunction() over the
// specified function company
$function = new ReflectionFunction('company');

// Calling the invoke() function
$A = $function->invoke('GeeksforGeeks',
            'is a Computer Science Portal.');

// Getting the result of the invoked function company
echo $A;
?>
```

**输出：**

```
GeeksforGeeks is a Computer Science Portal.

```

**程序 _2：**

```
<?php

// Initializing some user-defined functions
function Trial1($First_Args, $Second_Args) {
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

function Trial2($First_Args, $Second_Args) {
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

// Using ReflectionFunction() over the above
// specified functions 
$function = new ReflectionFunction('Trial1');
$function = new ReflectionFunction('Trial2');

// Calling the invoke() function and getting the
// result of the invoked function company
echo $function->invoke('a+a', '= 2a');
echo $function->invoke('a*a', '= a^2');
?>
```

**输出：**

```
a+a = 2a
a*a = a^2

```

**引用：**[https://www.php.net/manual/en/reflectionfunction.invoke.php](https://www.php.net/manual/en/reflectionfunction.invoke.php)