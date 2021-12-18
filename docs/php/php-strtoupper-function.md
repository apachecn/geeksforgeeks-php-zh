# PHP|stroupper()函数

> Original: [https://www.geeksforgeeks.org/php-strtoupper-function/](https://www.geeksforgeeks.org/php-strtoupper-function/)

函数的作用是：将字符串转换为大写。 此函数接受字符串作为参数，并将字符串中出现的所有小写英语字母转换为大写。 字符串中的所有其他数字字符或特殊字符保持不变。

**语法**：

```
*string* strtoupper ( $string )

```

**参数**：此函数的唯一参数是要转换为大写的字符串。

**返回值**：此函数返回所有字母都为大写的字符串。

例如：

```
Input : $str  = "GeeksForGeeks"
        strtoupper($str)
Output: GEEKSFORGEEKS

Input : $str  = "going BACK he SAW THIS 123$#%"
        strtoupper($str)
Output: GOING BACK HE SAW THIS 123$#%

```

下面的程序说明了 PHP 中的 stroupper()函数：

**程序 1**

```
<?php

// original string
$str = "GeeksForGeeks";

// string converted to upper case
$resStr = strtoupper($str);

print_r($resStr);

?>
```

产出：

```
GEEKSFORGEEKS

```

**程序 2**

```
<?php

// original string
$str = "going BACK he SAW THIS 123$#%";

// string to upper case
$resStr = strtoupper($str);

print_r($resStr);

?>
```

产出：

```
GOING BACK HE SAW THIS 123$#%

```

**参考**：
[http://php.net/manual/en/function.strtoupper.php](http://php.net/manual/en/function.strtoupper.php)