# PHP|ReflectionFunction InvokeArgs()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionfunction-invokeargs-function/](https://www.geeksforgeeks.org/php-reflectionfunction-invokeargs-function/)

**ReflectionFunction：：InvokeArgs()函数**是 PHP 中的内置函数，用于返回调用的函数调用的结果。

**语法：**

```php
*mixed* ReflectionFunction::invokeArgs( *array* $args )
```

**参数：**此函数接受单个参数**$args**，该参数保存传递给被调用函数的参数数组。

**返回值：**此函数返回调用的函数调用的结果。

下面的程序演示了 PHP 中的 ReflectionFunction：：InvokeArgs()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined function
function Company($Company_Name, $Role) {
    return sprintf("%s %s\r\n", $Company_Name, $Role);
}

// Using ReflectionFunction() over the specified
// function company
$function = new ReflectionFunction('company');

// Calling the invokeArgs() function
$A = $function->invokeArgs(array('GeeksforGeeks',
                 'is a Computer Science Portal.'));

// Getting the result of the invoked
// function company
echo $A;
?>
```

**输出：**

```php
GeeksforGeeks is a Computer Science Portal.

```

**程序 _2：**

```php
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

// Calling the invokeArgs() function and the
// result of the invoked function company
echo $function->invokeArgs(array('a+a', '= 2a'));
echo $function->invokeArgs(array('a*a', '= a^2'));
?>
```

**输出：**

```php
a+a = 2a
a*a = a^2

```

**引用：**[https://www.php.net/manual/en/reflectionfunction.invokeargs.php](https://www.php.net/manual/en/reflectionfunction.invokeargs.php)