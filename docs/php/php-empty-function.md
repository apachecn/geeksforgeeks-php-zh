# PHP|EMPTY()函数

> Original: [https://www.geeksforgeeks.org/php-empty-function/](https://www.geeksforgeeks.org/php-empty-function/)

Empty()函数是 PHP 中的内置函数，用于检查变量是否为空。

**语法：**

```php
bool empty ( $var )

```

**参数：**此函数接受单个参数，如上述语法所示，如下所述。

*   The **$var:** variable checks whether it is empty.

**注意：**在 PHP 5.5 以下的版本中，Empty()只支持变量，否则将导致解析错误。 以下语句将不起作用*Empty(Trim($var))*。 相反，可以使用*Trim($name)==false*。

**返回值：**如果$var 存在并且具有非空、非零值，则返回 FALSE。 否则返回 TRUE。

这些值被视为空值：

*   "" (empty string)
*   0 (0 for integer)
*   0.0 (0 for floating point)
*   "0" (0 for string)
*   无约束力的 / 无效的
*   与事实不符的 / 错的 / 貌似的 / 故意捏造的
*   Array () (empty array)

下面的程序演示了 PHP 中的 Empty()函数：

```php
<?php
// PHP code to demonstrate working of empty() function
$var1 = 0;
$var2 = 0.0;
$var3 = "0";
$var4 = NULL;
$var5 = false;
$var6 = array();
$var7 = "";

// for value 0 as integer
empty($var1) ? print_r("True\n") : print_r("False\n");

// for value 0.0 as float
empty($var2) ? print_r("True\n") : print_r("False\n");

// for value 0 as string
empty($var3) ? print_r("True\n") : print_r("False\n");

// for value Null
empty($var4) ? print_r("True\n") : print_r("False\n");

// for value false
empty($var5) ? print_r("True\n") : print_r("False\n");

// for array
empty($var6) ? print_r("True\n") : print_r("False\n");

// for empty string
empty($var7) ? print_r("True\n") : print_r("False\n");

// for not declare $var8
empty($var8) ? print_r("True\n") : print_r("False\n");

?>
```

**输出：**

```php
True
True
True
True
True
True
True
True

```

**引用：**[http://php.net/manual/en/function.empty.php](http://php.net/manual/en/function.empty.php)