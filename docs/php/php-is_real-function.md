# PHP|is_real()函数

> Original: [https://www.geeksforgeeks.org/php-is_real-function/](https://www.geeksforgeeks.org/php-is_real-function/)

**is_real()函数**是 PHP 中的一个内置函数，用于检查给定值是否为实数。

**语法：**

```
bool is_real( mixed $var )
```

**参数：**此函数接受一个参数，如上所述，如下所述：

*   **$var:** it contains the value of the variable to check.

**返回值：**如果变量的给定值为实数，则返回 TRUE，否则返回 FALSE。

**程序 1：**

```
<?php 
// PHP code to demonstrate
// the is_real() function

function square($num) { 
    return (is_real($num)); 
} 

var_dump(square(9.09)); 
var_dump(square(FALSE));
var_dump(square(14));
var_dump(square(56.30));

?> 
```

**Output:**

```
bool(true)
bool(false)
bool(false)
bool(true)

```

**程序 2：**

```
<?php 
// PHP program to demonstrate the
// is_real() function

$variable_name1 = 67.099; 
$variable_name2 = 32; 
$variable_name3 = "abc"; 
$variable_name4 = FALSE; 

// Check given variable is real number or not
if (is_real($variable_name1)) 
    echo "$variable_name1 is a real value. \n"; 
else
    echo "$variable_name1 is not a real value. \n"; 

// Check given variable is real number or not
if (is_float($variable_name2)) 
    echo "$variable_name2 is a real value. \n"; 
else
    echo "$variable_name2 is not a real value. \n"; 

// Check given variable is real number or not 
if (is_float($variable_name3)) 
    echo "$variable_name3 is a real value. \n"; 
else
    echo "$variable_name3 is not a real value. \n"; 

// Check given variable is real number or not
if (is_float($variable_name4)) 
    echo "FALSE is a real value. \n"; 
else
    echo "FALSE is not a real value. \n"; 
?> 
```

**输出：**

```
67.099 is a real value. 
32 is not a real value. 
abc is not a real value. 
FALSE is not a real value.

```

**引用：**[https://www.php.net/manual/en/function.is-real.php](https://www.php.net/manual/en/function.is-real.php)