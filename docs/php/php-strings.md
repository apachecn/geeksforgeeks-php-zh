# PHP|字符串

> Original: [https://www.geeksforgeeks.org/php-strings/](https://www.geeksforgeeks.org/php-strings/)

可以将字符串视为字符流。 例如，‘G’是一个字符，‘GeeksforGeek’是一个字符串。 我们已经在[PHP|数据类型和变量](https://www.geeksforgeeks.org/php-variables-data-types/)中了解了 PHP 中字符串数据类型的基础知识。

在本文中，我们将详细讨论字符串。 PHP 中的引号、单引号(‘’)和双引号(“”)中的所有内容都被视为字符串。

**创建字符串：**
在 PHP 中创建字符串有四种方式：

**1.单引号字符串**：这种类型的字符串不处理引号内的特殊字符。

## PHP

```php
<?php

// single-quote strings

$site  = 'Welcome to GeeksforGeeks';

echo $site;

?>
```

**输出：**

```php
Welcome to GeeksforGeeks
```

上述程序编译正确。 我们已经创建了一个字符串‘Welcome to GeeksforGeek’，并将其存储在变量中，并使用[*ECHO*](https://www.geeksforgeeks.org/php-echo-print/)语句打印它。(
现在让我们看看下面的程序：

## PHP

```php
<?php

// single-quote strings

$site  = 'GeeksforGeeks';

echo 'Welcome to $site';

?>
```

**输出：**

```php
Welcome to $site
```

在上面的程序中，*ECHO*语句打印变量名，而不是打印变量的内容。 这是因为 PHP 中的单引号字符串不处理特殊字符。 因此，字符串无法将‘{content}#x2019；’符号标识为变量名的开头。

**2.双引号字符串**：与单引号字符串不同，PHP 中的双引号字符串能够处理特殊字符。

## PHP

```php
<?php

// double-quote strings

echo "Welcome to GeeksforGeeks \n";

$site  = "GeeksforGeeks";

echo "Welcome to $site";

?>
```

**输出：**

```php
Welcome to GeeksforGeeks
Welcome to GeeksforGeeks
```

在上面的程序中，我们可以看到双引号字符串正在根据特殊字符的属性处理它们。 不打印‘\n’字符，并将其视为新行。 同样，打印的不是变量名$site，而是“GeeksforGeek”。

PHP 将双引号(“”)中的所有内容都视为字符串。

在本文中，我们将了解各种字符串函数的工作原理，以及如何实现它们以及字符串的一些特殊属性。 与整数、双精度等其他数据类型不同，字符串没有任何固定的限制或范围。 只要在引号内，它就可以扩展到任何长度。
前面已经讨论过，带单引号和双引号的字符串有不同的处理方式。 单引号中的字符串忽略特殊字符，但双引号字符串识别特殊字符并以不同方式对待它们。

**示例：**

## PHP

```php
<?php

$name = "Krishna";
echo "The name of the geek is $name \n";
echo 'The name of the geek is $name';

?>
```

**输出：**

```php
The name of the geek is Krishna 
The name of the geek is $name
```

下面介绍一些用于双引号字符串的重要且常用的特殊字符：

以反斜杠(“\”)开头的字符被视为转义序列，并替换为特殊字符。 以下是几个重要的转义序列。

1.  “\n”由新行替换
2.  “\t”替换为制表符空格
3.  “\{Content}#x201D；替换为美元符号
4.  “\r”替换为回车符
5.  “\\”替换为反斜杠
6.  “\”“替换为双引号
7.  “\‘”替换为单引号

*   以美元符号(“{content}#x201D；)开头的字符串被视为变量，并替换为变量的内容。

**3.Heredoc：**Heredoc(<<<)的语法是分隔 PHP 字符串的另一种方式。 在 herdoc(<<<)运算符之后给出一个标识符，之后可以在新行开始时写入任何文本。 为了结束语法，给出了相同的标识符，没有任何制表符或空格。

**注意：**Heredoc 语法类似于双引号字符串，不带引号。

**示例：**

## PHP

```php
<?php

 $input  = <<<testHeredoc

Welcome to GeeksforGeeks.
Started content writing in GeeksforGeeks!.
I am enjoying this.

testHeredoc;

echo $input;

?>
```

发帖主题：Re：Колибри0.7.0

```php
Welcome to GeeksforGeeks.
Started content writing in GeeksforGeeks!.
I am enjoying this.
```

**4.Nowdoc：**Nowdoc 与 HERDOC 非常相似，不同之处在于 HERDOC 中所做的解析。 *语法类似于 here doc 语法，符号<<<后跟用单引号括起的标识符。 Nowdoc 的规则与 here doc 相同。

**注意：**Nowdoc 语法类似于单引号字符串。

**示例：**

## PHP

```php
<?php

$input = <<<'testNowdoc'

Welcome to GeeksforGeeks.
Started content writing in GeeksforGeeks!.

testNowdoc;

echo $input;

// Directly printing string without any variable
echo <<<'Nowdoc'
<br/>
Welcome to GFG .
Learning PHP is fun in GFG.

Nowdoc;

?>
```

发帖主题：Re：Колибри0.7.0

```php
Welcome to GeeksforGeeks.
Started content writing in GeeksforGeeks!.

Welcome to GFG .
Learning PHP is fun in GFG. 
```

**内置字符串函数**

PHP 中的内置函数是一些现有的库函数，可以直接在我们的程序中使用，并对它们进行适当的调用。 下面是我们在日常和常规程序中使用的一些重要的内置字符串函数：

**1.strlen()函数**：该函数用于查找字符串的长度。 此函数接受字符串作为参数，并返回字符串的长度或字符数。

**示例：**

## PHP

```php
<?php

echo strlen("Hello GeeksforGeeks!");

?>
```

**输出：**

```php
20
```

**2.strrev()函数**：该函数用于反转字符串。 此函数接受字符串作为参数，并返回其反转的字符串。

**示例：**

## PHP

```php
<?php

echo strrev("Hello GeeksforGeeks!");

?>
```

**输出：**

```php
!skeeGrofskeeG olleH
```

**3.str_place()函数：**该函数接受三个字符串作为参数。 第三个参数是原始字符串，第一个参数被第二个参数替换。 换句话说，我们可以说它用第二个参数替换了原始字符串中所有出现的第一个参数。

**示例：**

## PHP

```php
<?php

echo str_replace("Geeks", "World", "Hello GeeksforGeeks!"), "\n";
echo str_replace("for", "World", "Hello GeeksforGeeks!"), "\n";

?>
```

**输出：**

```php
Hello WorldforWorld!
Hello GeeksWorldGeeks!
```

在第一个例子中，我们可以看到在“Hello GeeksforGeek！”中所有出现的单词“Geek”都被替换为“World”。

**4.strpos()函数：**该函数接受两个字符串参数，如果第一个字符串中存在第二个字符串，它将返回字符串的起始位置，否则返回 False。

**示例：**

## PHP

```php
<?php

echo strpos("Hello GeeksforGeeks!", "Geeks"), "\n";

echo strpos("Hello GeeksforGeeks!", "for"), "\n";

var_dump(strpos("Hello GeeksforGeeks!", "Peek"));

?>
```

**输出：**

```php
6
11
bool(false)
```

我们可以在上面的程序中看到，在第三个示例中，字符串“peek”不存在于第一个字符串中，因此该函数返回布尔值 FALSE，表示该字符串不存在。

**5.trim()函数：**该函数允许我们删除字符串两边的空格或字符串。

**示例：**

## PHP

```php
<?php

echo trim("Hello World!", "Hed!");

?>
```

发帖主题：Re：Колибри0.7.0

```php
llo Worl
```

**6.explode()函数：**此函数将字符串转换为数组。

**示例：**

## PHP

```php
<?php

$input  = "Welcome to geeksforgeeks";

print_r(explode(" ",$input));

?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [0] => Welcome [1] => to [2] => geeksforgeeks )
```

**7.strtolower()函数：**此函数将字符串转换为小写字符串。

**示例：**

## PHP

```php
<?php

$input  = "WELCOME TO GEEKSFORGEEKS";

echo strtolower($input);

?>
```

发帖主题：Re：Колибри0.7.0

```php
welcome to geeksforgeeks
```

**8.stroupper()函数：**此函数将字符串转换为大写字符串。

**示例：**

## PHP

```php
<?php

$input  = "Welcome to geeksforgeeks";

echo strtoupper($input);

?>
```

发帖主题：Re：Колибри0.7.0

```php
WELCOME TO GEEKSFORGEEKS
```

**9.strwordcount()函数：**此函数统计字符串中的总字数。

**示例：**

## PHP

```php
<?php

$input  = "Welcome to GeeksforGeeks";

echo str_word_count($input);

?>
```

发帖主题：Re：Колибри0.7.0

```php
3
```

**10.substr()函数：**该函数给出给定索引中给定字符串的子字符串。

**示例：**

## PHP

```php
<?php

$input  = "Welcome to geeksforgeeks";

echo(substr($input,3));

?>
```

发帖主题：Re：Колибри0.7.0

```php
come to geeksforgeeks
```

[**最近有关 PHP 字符串的文章**](https://www.geeksforgeeks.org/tag/php-string/)

本文由[**Chinmoy Lenka**](https://auth.geeksforgeeks.org/profile.php?user=lenkachinmoy)贡献。 如果你喜欢 GeeksforGeek 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章，或者把你的文章邮寄到 Contribute@geeksforgeeks.org。 看看你的文章出现在 GeeksforGeek 主页上，并帮助其他 Geek。
如果您发现任何不正确的地方，或者您想分享有关上述主题的更多信息，请写下评论。