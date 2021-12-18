# PHP|ReflectionFunction export()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionfunction-export-function/](https://www.geeksforgeeks.org/php-reflectionfunction-export-function/)

**ReflectionFunction：：Export()函数**是 PHP 中的一个内置函数，用于在返回参数设置为 true 时以字符串形式返回导出，否则返回 NULL。

**语法：**

```php
*string* ReflectionFunction::export( *string* $name, *string* $return )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name:** it is the specified function to export.
*   **$return:** it is a Boolean TRUE or FALSE. If its value is set to True, it will be exported, and if its value is set to False, it will return NULL. False is the default.

**返回值：**如果返回参数设置为 true，则此函数以字符串形式返回导出，否则返回 NULL。

下面的程序演示了 PHP 中的 ReflectionFunction：：Export()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined function
function Company($Company_Name, $Role) {
    return sprintf("%s %s\r\n", $Company_Name, $Role);
}

// Using ReflectionFunction() over the specified function company
$function = new ReflectionFunction('company');

// Calling the export() function
$A = $function->export(Company, $return = TRUE);

// Getting the export as a string
echo $A;
?>
```

**输出：**

```php
Function [ <user> function Company ] {
  @@ /home/b38c7d194c961e6b0d1d5b1c6e582d19.php 4 - 7

  - Parameters [2] {
    Parameter #0 [ <required> $Company_Name ]
    Parameter #1 [ <required> $Role ]
  }
}

```

**程序 2：**

```php
<?php

// Initializing some user-defined functions
function Trial1($First_Args, $Second_Args) {
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

function Trial2($First_Args, $Second_Args) {
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

// Using ReflectionFunction() over the above specified functions 
$function1 = new ReflectionFunction('Trial1');
$function2 = new ReflectionFunction('Trial2');

// Calling the export() function and
// Getting the export as a string
echo $function1->export(Trial1, $return = TRUE);
echo $function2->export(Trial2, $return = FALSE);
?>
```

**输出：**

```php
Function [ <user> function Trial1 ] {
  @@ /home/2410abe3ca2b5235249f9a0c9ba035b4.php 4 - 7

  - Parameters [2] {
    Parameter #0 [ <required> $First_Args ]
    Parameter #1 [ <required> $Second_Args ]
  }
}
Function [ <user> function Trial2 ] {
  @@ /home/2410abe3ca2b5235249f9a0c9ba035b4.php 9 - 12

  - Parameters [2] {
    Parameter #0 [ <required> $First_Args ]
    Parameter #1 [ <required> $Second_Args ]
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectionfunction.export.php](https://www.php.net/manual/en/reflectionfunction.export.php)