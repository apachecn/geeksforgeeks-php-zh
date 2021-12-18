# PHP|Soundex()函数

> Original: [https://www.geeksforgeeks.org/php-soundex-function/](https://www.geeksforgeeks.org/php-soundex-function/)

Soundex()函数是 PHP 中的内置函数，用于计算给定字符串的[Soundex 键](https://en.wikipedia.org/wiki/Soundex)。

Soudex 键是一个四字符长的字母数字字符串(以字母开头)，表示给定字符串的英语发音。

**语法**：

```
*string* soundex($str);

```

**参数**：此函数接受单个参数*$str*，该参数表示我们要为其查找 Soundex 键的字符串。

**返回值**：它以字符串形式返回 Soundex 键。

以下程序说明了 PHP 中的 Soundex()函数：

**程序 1：**在下面的程序中，Soudex()函数生成字符串“geeksforgeek”的 Soundex 键。

```
<?php

$str = "geeksforgeeks";

echo soundex($str);

?>
```

产出：

```
G216

```

**程序 2：**在下面的程序中，我们将看到两个发音相同的单词产生相似的发音键。

```
<?php

$str1 = "hair";
$str2 = "heir";

echo soundex($str1)."\n";
echo soundex($str2);

?>
```

产出：

```
H600
H600

```

**参考**：
[http://php.net/manual/en/function.soundex.php](http://php.net/manual/en/function.soundex.php)