# PHP|print_r()函数

> Original: [https://www.geeksforgeeks.org/php-print_r-function/](https://www.geeksforgeeks.org/php-print_r-function/)

Print_r()函数是 PHP 中的内置函数，用于打印或显示存储在变量中的信息。

**语法**：

```
print_r( $variable, $isStore )
```

**参数**：此函数接受两个参数，如上面的语法所示，如下所述。

1.  **$VARIABLE**：该参数指定要打印的变量，是必选参数。
2.  **$isStore**：这是一个选项参数。 该参数是布尔类型，其默认值为 false，用于将 print_r()函数的输出存储在变量中，而不是打印出来。 如果该参数设置为 true，则 print_r()函数将返回它应该打印的输出。

**返回值**：如果$Variable 是整数、浮点数或字符串，则函数打印变量的值。 如果变量是数组，则函数以显示键和值的格式打印数组，对象使用类似的表示法。

以下程序说明了 print_r()函数：

**程序 1**：

```
<?php

// PHP program to illustrate
// the print_r() function

// string variable
$var1 = "Welcome to GeeksforGeeks";

// integer variable
$var2 = 101;

// array variable
$arr = array('0' => "Welcome", '1' => "to", '2' => "GeeksforGeeks");

// printing the variables
print_r($var1);
echo"\n";
print_r($var2);
echo"\n";
print_r($arr);

?>
```

产出：

```
Welcome to GeeksforGeeks
101
Array
(
    [0] => Welcome
    [1] => to
    [2] => GeeksforGeeks
)

```

**程序 2**：

```
<?php

// PHP program to illustrate the print_r()
// function when $isStore is set to true

// array variable
$arr = array('0' => "Welcome", '1' => "to",
                     '2' => "GeeksforGeeks");

// storing output of print_r() function
// in another variable
$results = print_r($arr, true); 

echo $results;

?>
```

产出：

```
Array
(
    [0] => Welcome
    [1] => to
    [2] => GeeksforGeeks
)

```

**参考**：
[http://php.net/manual/en/function.print-r.php](http://php.net/manual/en/function.print-r.php)