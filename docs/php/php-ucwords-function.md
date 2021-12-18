# PHP|ucwords()函数

> Original: [https://www.geeksforgeeks.org/php-ucwords-function/](https://www.geeksforgeeks.org/php-ucwords-function/)

Ucwords()函数是 PHP 中的一个内置函数，用于将字符串中每个单词的第一个字符转换为大写。

**语法**：

```php
*string* ucwords ( $string, $separator )

```

**参数**：该函数接受两个参数，第一个是必选的，第二个是可选的。 下面对这两个参数进行说明：

1.  **$string**：这是要将每个单词的第一个字符转换为大写的输入字符串。
2.  **$分隔符**：这是一个可选参数。 此参数指定将用作输入字符串中单词分隔符的字符。 例如，如果分隔符是‘|’，而输入字符串是“Hello|world”，则表示该字符串包含两个单词“Hello”和“world”。

**返回值**：此函数返回每个单词都以大写字母开头的字符串。

例如：

```php
Input : $str  = "Geeks for geeks"
        ucwords($str)
Output: Geeks For Geeks

Input : $str  = "going BACK he SAW THIS"
        ucwords($str)
Output: Going BACK He SAW THIS

```

下面的程序演示了 PHP 中的 ucword()函数：

**程序 1**：

```php
<?php

// original string
$str  = "Geeks for geeks";

// string after converting first character
// of every word to uppercase
$resStr = ucwords($str);

print_r($resStr);

?>
```

产出：

```php
Geeks For Geeks

```

**程序 2**：

```php
<?php

// original string
$str = "Geeks#for#geeks #PHP #tutorials";

$separator = '#';

// string after converting first character
// of every word to uppercase
$resStr = ucwords($str, $separator);

print_r($resStr);

?>
```

产出：

```php
Geeks#For#Geeks #PHP #Tutorials

```

**注意**：您不应该使用字符‘{content}#x2019；’作为分隔符，因为 PHP 中任何以$开头的名称都被视为变量名。 因此，您的程序可能会给出一个找不到变量的错误。

**参考**：
[http://php.net/manual/en/function.ucwords.php](http://php.net/manual/en/function.ucwords.php)