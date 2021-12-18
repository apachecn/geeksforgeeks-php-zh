# PHP|is_null()函数

> Original: [https://www.geeksforgeeks.org/php-is_null-function/](https://www.geeksforgeeks.org/php-is_null-function/)

Is_null()函数是 PHP 中的一个内置函数，用于确定变量是否为空。

**语法：**

```
 boolean is_null ( $var )
```

**参数：**此函数接受单个参数，如上述语法所示，如下所述。

*   **$var：**变量检查是否为空。

**返回值：**它返回布尔值。 也就是说，当$var 为空时返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 is_null()函数：

**程序 1：**

## PHP

```
<?php
// PHP code to demonstrate the working of is_null() function
$var1 = NULL;
$var2 = "\0"; // "\0" means "\0"
$var3 = "NULL";
$var4 = 0;

// $var1 has NULL value, so always give TRUE
is_null($var1) ? print_r("True\n") : print_r("False\n");

// $var2 has '\0' value which consider as null in
// c and c++ but here taken as string, gives FALSE
is_null($var2) ? print_r("True\n") : print_r("False\n");

// $var3 has NULL string value so it will false
is_null($var3) ? print_r("True\n") : print_r("False\n");

// $var4 is 0, gives FALSE
is_null($var4) ? print_r("True\n") : print_r("False\n");

?>
```

发帖主题：Re：Колибри0.7.8.0

```
True
False
False
False
```

**程序 2：**

## PHP

```
<?php
// PHP code to demonstrate the working of
// is_null() function

function check_null($var)
{
    return (is_null($var) ? "True" : "False");
}

echo check_null(NULL) . "\n";
echo check_null(null) . "\n";
echo check_null(Null) . "\n";
echo check_null(NUll) . "\n";
echo check_null(NULl) . "\n";
echo check_null(nulL) . "\n";
echo check_null(nuLL) . "\n";
echo check_null(nULL) . "\n";

echo check_null(Nul) . "\n";
echo check_null(false) . "\n";

?>
```

发帖主题：Re：Колибри0.7.8.0

```
True
True
True
True
True
True
True
True
False
False
```

**引用：**[http://php.net/manual/en/function.is-null.php](http://php.net/manual/en/function.is-null.php)