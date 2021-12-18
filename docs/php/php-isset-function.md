# PHP|isset()函数

> Original: [https://www.geeksforgeeks.org/php-isset-function/](https://www.geeksforgeeks.org/php-isset-function/)

**isset()函数**是 PHP 中的一个内置函数，用于确定变量是否已声明且其值是否不等于 NULL。

**语法：**

```php
bool isset( mixed $var [, mixed $... ] )
```

**参数：**此函数接受一个或多个参数，如上所述，如下所述：

*   **$var:** it contains variables that need to be checked.
*   **{Content} # x2026 * *:** contains a list of other variables.

**返回值：**如果 var 存在，则返回 TRUE，否则其值不等于 NULL，否则返回 FALSE。

下面的示例说明了 PHP 中的 isset()函数：

**示例 1：**

```php
<?php

$str = "GeeksforGeeks";

// Check value of variable is set or not
if(isset($str)) {
    echo "Value of variable is set";
}
else {
    echo "Value of variable is not set";
}

$arr = array();

// Check value of variable is set or not
if( !isset($arr[0]) ) {
    echo "\nArray is Empty";
}
else {
    echo "\nArray is not empty";
}

?>
```

**输出：**

```php
Value of variable is set
Array is Empty

```

发帖主题：Re：Колибри0.7.0

**示例 2：**

```php
<?php

$num = 21;
var_dump(isset($num));

$arr = array(
        "a" => "Welcome",
        "b" => "to",
        "c" => "GeeksforGeeks"
    );

var_dump(isset($arr["a"]));
var_dump(isset($arr["b"]));
var_dump(isset($arr["c"]));
var_dump(isset($arr["Geeks"]));

?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/function.isset.php](https://www.php.net/manual/en/function.isset.php)