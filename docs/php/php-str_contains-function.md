# PHP STR_CONTAINS()函数

> Original: [https://www.geeksforgeeks.org/php-str_contains-function/](https://www.geeksforgeeks.org/php-str_contains-function/)

**STR_CONTAINS()**是 PHP 8 发布时引入的预定义函数。STR_CONTAINS()函数在表达式中搜索给定字符串中的子字符串。 如果提到的子字符串将出现在字符串中，则它将返回 True，否则将返回 False。 STR_CONTAINS()函数与 strpos()函数非常相似。

#### 物业：

1.  它始终返回布尔值。
2.  如果检查该子字符串是否为空，则返回 TRUE。
3.  它区分大小写。
4.  此函数是二进制安全的。
5.  它仅在 PHP 8 或更高版本上受支持。

#### 语法：

```php
(str_contains('String', 'Substring')) ;
```

子字符串是需要搜索的字符串，而字符串是要搜索子字符串的部分。

#### 注意：STR_CONTAINS()仅在 PHP 8 或更高版本中受支持。

**示例：**在下面的示例中，我们有一个句子存储在**$语句**中，一个单词存储在**$WORD**中。 在本例中，我们试图通过使用 str_concludes()函数检查单词是否出现在句子中。 如果单词将出现在句子***‘is’***将被赋给**$Result**，否则它的值将是***‘is*****Not**’。 我们将使用示例来理解这一点。

## PHP

```php
<?php

$sentence = 'GFG is Awesome';
$word = 'GFG';

$result = str_contains($sentence, $word) ? 'is' : 'is not';

echo "The word {$word} {$result} present in the sentence \"{$sentence}\" ";

?>
```

通过上面的内容，我们已经了解了如何通过使用 str_concludes()函数在给定字符串中查找子字符串&返回值将是布尔值。

#### 发帖主题：Re：Колибри0.7.0

```php
The word GFG is present in the sentence "GFG is Awesome"
```

**引用：**[https://www.php.net/manual/en/function.str-contains.php](https://www.php.net/manual/en/function.str-contains.php)