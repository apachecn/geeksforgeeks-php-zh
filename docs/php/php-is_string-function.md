# PHP|is_string()函数

> Original: [https://www.geeksforgeeks.org/php-is_string-function/](https://www.geeksforgeeks.org/php-is_string-function/)

**is_string()函数**是 PHP 中的一个内置函数，用于检查给定值是否为字符串。

**语法：**

```
bool is_string( mixed $var )
```

**参数：**此函数接受一个参数，如上所述，如下所述：

*   **$var:** it contains values that need to be checked.

**返回值：**如果变量的值是字符串类型，则返回 TRUE，否则返回 FALSE。

**程序 1：**

```
<?php

$str = "GeeksforGeeks";

// Check value of variable is set or not
if(is_string($str)) {
    echo "String";
}
else {
    echo "Not String";
}

$arr = array(10, 25.56, 'G', true, 'Geeks');

foreach ($arr as $index) {
    if(is_string($index)) {
        echo "\nString";
    }
    else {
        echo "\nNot String";
    }
}

?>
```

**Output:**

```
String
Not String
Not String
String
Not String
String

```

**程序 2：**

```
<?php

$num = 21;
var_dump(is_string($num));

$arr = array(
        "a" => "Welcome",
        "b" => 2,
        "c" => "GeeksforGeeks"
    );

var_dump(is_string($arr["a"]));
var_dump(is_string($arr["b"]));
var_dump(is_string($arr["c"]));

?>
```

**输出：**

```
bool(false)
bool(true)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/function.is-string.php](https://www.php.net/manual/en/function.is-string.php)