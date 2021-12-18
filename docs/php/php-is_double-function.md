# PHP|is_double()函数

> Original: [https://www.geeksforgeeks.org/php-is_double-function/](https://www.geeksforgeeks.org/php-is_double-function/)

Is_double()函数是 PHP 中的一个内置函数，用于确定给定值是否为双精度值。

**语法：**

```php
bool is_double( $variable_name )
```

**参数：**此函数接受一个参数，如上所述，如下所述：

*   **$Variable_NAME:** this parameter holds the value that needs to be checked.

**返回值：**它是一个布尔值，即如果$VARIABLE_NAME CONTAINS 为双精度值，则为 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 is_double()函数：

**程序 1：**

```php
<?php 
// PHP code to implement is_double() 
// function

function square($num) 
{ 
    return (is_double($num)); 
} 

echo square(9.09) ."\n"; // outputs '1'. 
echo square(FALSE) ."\n"; // gives no output. 
echo square(14) ."\n"; // gives no output. 
echo square(56.30) ."\n"; // outputs '1' 

?> 
```

**输出：**

```php
1

1

```

**程序 2：**

```php
<?php 
// PHP code to implement is_double()
// function

$variable_name1 = 67.099; 
$variable_name2 = 32; 
$variable_name3 = "abc"; 
$variable_name4 = FALSE; 

// $variable_name1 is double value, gives TRUE 
if (is_double($variable_name1)) 
    echo "$variable_name1 is a double value. \n"; 
else
    echo "$variable_name1 is not a double value. \n"; 

// $variable_name2 is not a double value, gives FALSE 
if (is_double($variable_name2)) 
    echo "$variable_name2 is a double value. \n"; 
else
    echo "$variable_name2 is not a double value. \n"; 

// $variable_name3 is not a double value, gives FALSE 
if (is_double($variable_name3)) 
    echo "$variable_name3 is a double value. \n"; 
else
    echo "$variable_name3 is not a double value. \n"; 

// $variable_name4 is not a double value, gives FALSE 
if (is_double($variable_name4)) 
    echo "FALSE is a double value. \n"; 
else
    echo "FALSE is not a double value. \n"; 
?> 
```

**输出：**

```php
67.099 is a double value. 
32 is not a double value. 
abc is not a double value. 
FALSE is not a double value.

```

**引用：**[https://www.php.net/manual/en/function.is-double.php](https://www.php.net/manual/en/function.is-double.php)