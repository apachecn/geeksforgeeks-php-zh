# PHP|IS_FLOAT()函数

> Original: [https://www.geeksforgeeks.org/php-is_float-function/](https://www.geeksforgeeks.org/php-is_float-function/)

**is_float()**是[PHP](https://www.geeksforgeeks.org/php/)中的内置函数。 函数的作用是：确定变量是否为浮点型。

**语法：**

```
 *boolean*  is_float($variable_name)
```

**参数**：此函数包含一个参数，如上面的语法和所述，如下所述

*   **$VARIABLE_NAME**：我们要检查的变量。

**返回值**：
它是一个布尔函数，因此当$VARIABLE_NAME 为整数时返回 TRUE，否则返回 FALSE。

下面的示例说明了函数 isFloat()的工作原理。

**示例 1：**：

```
<?php

// php code demonstrate working of is_float()
$variable_name1 = 67.099;
$variable_name2 = 32;
$variable_name3 = "abc";
$variable_name4 = FALSE;

// $variable_name1 is float, gives TRUE
if (is_float($variable_name1))
    echo "$variable_name1 is a float value. \n";
else
    echo "$variable_name1 is not a float value. \n";

// $variable_name2 is not float, gives FALSE
if (is_float($variable_name2))
    echo "$variable_name2 is a float value. \n";
else
    echo "$variable_name2 is not a float value. \n";

// $variable_name3 is not float, gives FALSE
if (is_float($variable_name3))
    echo "$variable_name3 is a float value. \n";
else
    echo "$variable_name3 is not a float value. \n";

// $variable_name4 is not float, gives FALSE
if (is_float($variable_name4))
    echo "FALSE is a float value. \n";
else
    echo "FALSE is not a float value. \n";
?>
```

发帖主题：Re：Колибри0.7.8.0

```
67.099 is a float value. 
32 is not a float value. 
abc is not a float value. 
FALSE is not a float value. 

```

**示例 2**：

```
<?php
// PHP code demonstrate working of is_float()

function square($num)
{
    return (is_float($num));
}

echo square(9.09) ."\n";  // outputs '1'.
echo square(FALSE) ."\n"; // gives no output.
echo square(14) ."\n";    // gives no output.
echo square(56.30) ."\n";  // outputs '1'

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1

1

```

**参考**：[http://php.net/manual/en/function.is-float.php](http://php.net/manual/en/function.is-float.php)