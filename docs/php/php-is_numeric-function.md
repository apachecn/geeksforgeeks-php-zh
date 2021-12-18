# PHP|is_numeric()函数

> Original: [https://www.geeksforgeeks.org/php-is_numeric-function/](https://www.geeksforgeeks.org/php-is_numeric-function/)

Is_numeric()函数是 PHP 中的一个内置函数，用于检查作为参数传入函数的变量是数字还是数字字符串。 该函数返回布尔值。

**语法：**

```
bool is_numeric ( $var )
```

**参数：**该函数接受单个参数，该参数是必选的，如下所述：

*   **$var：**此输入参数是函数检查其是数字还是数字字符串的变量。 基于此验证，该函数返回一个布尔值。

**返回值：**如果$var 是数字或数字字符串，则函数返回*true*，否则返回*false*。

**示例：**

```
Input : $var = 12
Output : True

Input : $var = "Geeks for Geeks"
Output : False
```

以下程序说明了 is_numeric()函数：

**程序 1：**在此程序中，数字作为输入传递。

## PHP

```
<?php

$num = 12;
if (is_numeric($num)) {
        echo $num . " is numeric";
    }
    else {
        echo $num . " is not numeric";
    }

?>
```

**Output:** 

```
12 is numeric
```

**程序 2：**在此程序中，字符串作为输入传递。

## PHP

```
<?php

$element = "Geeks for Geeks";
if (is_numeric($element)) {
        echo $element . " is numeric";
    }
    else {
        echo $element . " is not numeric";
    }

?>
```

**Output:** 

```
Geeks for Geeks is not numeric
```

**程序 3：**在此程序中，数字字符串作为输入传递。

## PHP

```
<?php

$num = "467291";
if (is_numeric($num)) {
        echo $num . " is numeric";
    }
    else {
        echo $num . " is not numeric";
    }

?>
```

**Output:** 

```
467291 is numeric
```

**程序 4：**

## PHP

```
<?php
$array = array(
    "21/06/2018",
    4743,
    0x381,
    01641,
   0b1010010011,
    "Geek Classes"
);

foreach ($array as $i) {
    if (is_numeric($i)) {
        echo $i . " is numeric"."\n";
    } else {
        echo $i . " is NOT numeric"."\n";
    }
}
?>
```

**Output:** 

```
21/06/2018 is NOT numeric
4743 is numeric
897 is numeric
929 is numeric
659 is numeric
Geek Classes is NOT numeric
```

**引用：**[http://php.net/manual/en/function.is-numeric.php](http://php.net/manual/en/function.is-numeric.php)