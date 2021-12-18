# PHP func_get_arg()函数

> Original: [https://www.geeksforgeeks.org/php-func_get_arg-function/](https://www.geeksforgeeks.org/php-func_get_arg-function/)

**func_get_arg()**函数是 PHP 中的一个内置函数，用于从作为参数传递的参数中获取提到的值。

**语法：**

```
*mixed* func_get_arg( *int* $arg )
```

**参数：**此函数接受单个参数，如上所述，如下所述。

*   $arg：此参数保存实参偏移量，其中通过假定第一个实参为 0 来计算参数中实参的偏移量。

**返回值：**此方法返回上述参数，如果出现错误则返回 False。

**示例 1：**

```
<?php

// Function definition
function geeks($a, $b, $c) {

    // Calling func_get_arg() function  
    echo "Print second argument: "
        . func_get_arg(1) . "\n";
}

// Function call
geeks('hello', 'php', 'geeks');

?>
```

发帖主题：Re：Колибри0.7.0

```
Print second argument: php
```

**什么时候发生错误？**
错误出现在两种情况下。

*   如果参数偏移量的值大于作为函数参数传递的参数的实际值。
*   如果此函数不是从用户定义函数内部调用的。

```
<?php

// Function definition
function geeks($a, $b, $c) {

    // Printing the sixth argument
    // that doesn't exist
    echo "Printing the sixth argument: "
        . func_get_arg(5) . "\n";
}

// Function call
geeks('hello', 'php', 'geeks');

?>
```

发帖主题：Re：Колибри0.7.0

```
Warning:  func_get_arg():  Argument 5 not passed to function in 
    [...][...] on line 4

```

**示例：**

```
<?php

// Function definition
function geeks($a, $b, $c) {
     $a = "Bye";
}

// Function call
geeks('hello', 'php', 'geeks');

// The func_get_arg() function
// is called from outside the
// user defined function
echo "Printing the sixth argument: "
        . func_get_arg(5) . "\n";

?>
```

发帖主题：Re：Колибри0.7.0

```
PHP Warning:  func_get_arg():  Called from the global scope - 
no function context in /home/main.php on line 9       

```

**对于 PHP 5.3 之前的版本：**获取函数的参数对于低于 5.3 的 PHP 版本有不同的方法。 所有 5.3 和 5.3 以上的版本都将显示以下代码的错误。

**示例：**

```
<?php
function geeks() {
    include './testing.inc';
}

geeks('Welcome', 'PHP', 'Geeks');
?>
```

**测试.inc：**

```
<?php

$parameter = func_get_arg(1);
var_export($parameter);

?>
```

发帖主题：Re：Колибри0.7.0

```
'PHP' warnings

```

**注意：**要获取多个参数，可以使用**func_get_args()**函数代替**func_get_arg()**函数。