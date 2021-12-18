# PHP|strrchr 函数

> Original: [https://www.geeksforgeeks.org/php-strrchr-function/](https://www.geeksforgeeks.org/php-strrchr-function/)

**strrchr()**函数是 PHP 中的内置函数。 此函数接受两个参数，一个字符串和一个字符。 此函数搜索给定字符串中的给定字符，并返回从该字符串中最后一次出现的给定字符开始的字符串部分。

**语法**：

```
strrchr($string, $key)

```

**参数**：此函数接受两个参数。 这两个参数都是必需的，说明如下：

*   **$string**：这是我们要在其中搜索给定键的输入字符串。
*   **$key**：该参数表示要在给定字符串$string 中搜索的字符。 如果此参数包含多个字符，则只会在$string 中搜索此参数的第一个字符。

**返回值**：此函数返回从该字符串中最后一次出现的给定$key 开始的$string 部分。

例如：

```
Input : $string = "Hello|welcome|to|gfg"  $key = '|'
Output : |gfg

Input :  $string = "Welcome\nto\ngfg"  $key = '\n'
Output : gfg

```

以下程序说明了 PHP 中的 strrchr()函数：

**程序 1**：

```
<?php

// Input string
$string = "Hello|welcome|to|gfg";

// key to be searched
$key = "|";

echo strrchr($string, $key);

?>
```

产出：

```
|gfg

```

**程序 2**：当$key 包含转义序列时。

```
<?php

// Input string
$string = "Hello\nwelcome\nto\ngfg";

// key to be searched
$key = "\n";

echo strrchr($string, $key);

?>
```

产出：

```

gfg

```

**程序 3**：当$key 包含多个字符时。

```
<?php

// Input string
$string = "Hello|welcome|to|gfg";

// key to be searched
$key = "|welcome";

echo strrchr($string, $key);

?>
```

产出：

```
|gfg

```

**参考**：
[http://php.net/manual/en/function.strrchr.php](http://php.net/manual/en/function.strrchr.php)