# PHP|nl2br()函数

> Original: [https://www.geeksforgeeks.org/php-nl2br-function/](https://www.geeksforgeeks.org/php-nl2br-function/)

Nl2br()是 PHP 中的一个内置函数，用于在字符串中所有新行的位置插入 HTML 换行符。 在普通文本编辑器中，新行通常使用以下任一项表示。

*   \n\r
*   \r\n
*   \n
*   \r

其中，**\n**建议将光标移至下一行，**\r**建议将光标移至行首。 此函数接受可能包含换行符的字符串，并通过在所有换行符序列前插入**br**标记返回更改后的字符串。 作为一种标记语言，HTML 不理解新行字符序列，这是该函数的用武之地。

**语法：**

```
nl2br($str, $isXHTML)

```

**参数**：该函数最多可带两个参数，如下所示。

*   **$str** : the string to change.
*   **$isXHTML** : this is an optional parameter and requires a Boolean value to indicate whether to use the XHTML compatible newline character, that is, whether to use < br/ >. The default value is true.

**返回类型**：此函数迭代输入字符串，并在每个换行符之前插入 br 标记，然后返回更改后的字符串。

以下程序说明了 nl2br()在 PHP 中的工作方式：

```
<?php

// PHP code to illustrate the working of nl2br()
$unaltered_string = "Hey There! Welcome.\n-GeeksforGeeks";
echo nl2br($unaltered_string);

?>
```

发帖主题：Re：Колибри0.7.0

帖子主题：Re：Колибри

**要注意的要点**：

*   It is used to display text stored in the database.
*   Different operating systems prefer to use different character sequences as newline characters, for example, Windows uses\ r\ n, while Linux uses\ nMagneMAC\ r.
*   Using simple string substitution can produce similar results, although keep in mind that the nl2br function does not replace the new line sequence.

**参考**：[http://php.net/manual/en/function.nl2br.php](http://php.net/manual/en/function.nl2br.php)