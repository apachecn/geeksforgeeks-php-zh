# PHP|ReflectionFunction__toString()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionfunction-__tostring-function/](https://www.geeksforgeeks.org/php-reflectionfunction-__tostring-function/)

**ReflectionFunction：：__toString()函数**是 PHP 中的内置函数，用于返回指定函数的字符串表示形式。

**语法：**

```
*string* ReflectionFunction::__toString( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定函数的字符串表示形式。

下面的程序演示了 PHP 中的 ReflectionFunction：：__toString()函数：

**程序 1：**

```
<?php

// Initializing a user-defined function
function Company($Company_Name, $Role)
{
    return sprintf("%s %s\r\n", $Company_Name, $Role);
}

// Using ReflectionFunction() over the specified
// function company
$function = new ReflectionFunction('company');

// Calling the __toString() function
$A = $function->__toString();

// Getting the string representation of the
// above specified function
echo $A;
?>
```

**输出：**

```
Function [ <user> function Company ] {
  @@ /home/a39c30763ecfc7f257d02e44de746b22.php 4 - 7

  - Parameters [2] {
    Parameter #0 [ <required> $Company_Name ]
    Parameter #1 [ <required> $Role ]
  }
}

```

**程序 2：**

```
<?php

// Initializing some user-defined functions
function Trial1($First_Args, $Second_Args)
{
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

function Trial2($First_Args, $Second_Args)
{
    return sprintf("%s %s\r\n", $First_Args, $Second_Args);
}

// Using ReflectionFunction() over the above
// specified functions 
$function = new ReflectionFunction('Trial1');
$function = new ReflectionFunction('Trial2');

// Calling the __toString() function and
// Getting string representation of the
// above specified funtion
echo $function->__toString();
echo $function->__toString();
?>
```

**输出：**

```
Function [ <user> function Trial2 ] {
  @@ /home/09f598906ca0bfcad4613b5dea41c27b.php 9 - 12

  - Parameters [2] {
    Parameter #0 [ <required> $First_Args ]
    Parameter #1 [ <required> $Second_Args ]
  }
}
Function [ <user> function Trial2 ] {
  @@ /home/09f598906ca0bfcad4613b5dea41c27b.php 9 - 12

  - Parameters [2] {
    Parameter #0 [ <required> $First_Args ]
    Parameter #1 [ <required> $Second_Args ]
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectionfunction.tostring.php](https://www.php.net/manual/en/reflectionfunction.tostring.php)