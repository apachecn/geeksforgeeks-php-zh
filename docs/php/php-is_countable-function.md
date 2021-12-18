# PHP|is_countable()函数

> Original: [https://www.geeksforgeeks.org/php-is_countable-function/](https://www.geeksforgeeks.org/php-is_countable-function/)

Is_countable()函数是 PHP 中的一个内置函数，用于检查变量的内容是否可计数。

**语法：**

```
bool is_countable ( mixed $var )
```

**参数：**此函数接受一个参数，如上所述，如下所述：

*   **$var:** this parameter holds the value that needs to be checked.

**返回值：**此函数返回布尔值，即如果变量的值可数，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的 is_countable()函数：

**程序 1：**

```
<?php

// Declare a string
$str = "GeeksforGeeks"; 

var_dump(is_countable($str));

$arr = array(1, 3, 5, 7);

var_dump(is_countable($arr));
?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Declare a number
$num = 1234;
var_dump(is_countable($num));

// Declare an array
$arr = array('Welcome', 'to', 'GeeksforGeeks');
var_dump(is_countable($arr));

// Declare a string
$str = "GeeksforGeeks"; 
var_dump(is_countable($str));

// Declare an empty class
class GFG {
    // Empty class
}

// Create an object of class
$obj = new GFG();
var_dump(is_countable($obj));

// Create an array iterator object
$itr = new ArrayIterator();
var_dump(is_countable($itr));
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.is-countable.php](https://www.php.net/manual/en/function.is-countable.php)