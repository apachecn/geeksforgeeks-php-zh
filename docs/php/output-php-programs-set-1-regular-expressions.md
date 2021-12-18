# PHP 程序输出|集合 1(正则表达式)

> 原文:[https://www . geesforgeks . org/output-PHP-programs-set-1-正则表达式/](https://www.geeksforgeeks.org/output-php-programs-set-1-regular-expressions/)

预测以下 PHP 程序的输出:

**问题 1**

```
<?php
    echo str_pad("Welcome", 5)." to GeeksforGeeks.";
?>
```

选项:

1.  Welcome to Geek Forum.
2.  Yeah, geek upstart. Welcome to Geek Forum
3.  . welcome
4.  Welcome to Geek Forum.

输出:

```
Welcome to GeeksforGeeks.

```

**解释:**str _ pad()函数用指定数量的字符填充字符串。

**问题 2**

```
<?php
    $author = "GeeksforGeeks";
    $author = str_replace("e","i",$author);
    echo "I am intern at $author.";
?>
```

选项:

1.  I'm GeeksforGeeks' intern.

2.  I'm GiiksforGiiks's intern.
3.  mistake

输出:

```
I am intern at GiiksforGiiks.

```

**解释:**str _ replace()函数区分大小写，将一个字符串的所有实例替换为另一个字符串。

**问题 3**

```
<?php
    $GfG = "GeeksforGeeks";
    echo ltrim(strstr($GfG, "f"),"f");
?>
```

选项:

*   【极客 forgeeks】*   【极客】*   【极客 sf】【管风琴】

输出:

```
orGeeks

```

**解释:**strtr()函数返回从预定义字符串的第一次出现开始的字符串的剩余部分。

**问题 4**

```
<?php
    $username = "sagarshUkla785";
    if (ereg("([^a-z])",$username))
        echo "Not a valid username!";
    else
        echo "Valid username!";
?>
```

选项:

1.  mistake
2.  Is not a valid user name!
3.  Valid user name!
4.  Do not return output

输出:

```
Not a valid username!

```

**解释:**由于提供的用户名不全是小写，ereg()不会返回 FALSE(而是返回匹配字符串的长度，PHP 会将其视为 TRUE)，导致消息输出。

**第五题**

```
<?php
    $GfG = "Hello\tWelcome to\nGeeksforGeeks.";
    print_r(split("[\n\t]",$GfG));
?>
```

选项:

1.  Hello, everyone. Welcome to GeeksforGeeks.

2.  [0] = > Hello [1] = > Welcome to [2] = > Geeks for Geeks.

输出:

```
[0] => Hello [1] => Welcome to [2] => GeeksforGeeks.

```

**解释:**split()函数将一个字符串划分为多个元素，每个元素的边界基于字符串中定义的模式的出现。

**第 6 题**

```
<?php
    $languages = array("C++", "JAVA", "PYTHON", "SCALA");
    $language = preg_grep("/^S/", $languages);
    print_r($language);
?>
```

选项:

1.  数组([0]= > c++[1]= > JAVA[2]= > PYTHON[3]= > SCALA)
2.  Array ([3] = > SCALA)
3.  Array ([1]=>JAVA)

输出:

```
Array ( [3] => SCALA )

```

**说明:**此函数用于在数组中搜索以 s 开头的语言。

**问题 7**

```
<?php
    $title = "i'm intern at geeksforGeeks.";
    echo ucwords($title);
?>
```

选项:

1.  I'm an intern at geek company.
2.  I'm an intern at geek company.
3.  I'm an intern at geek company.
4.  I'm an intern at geek company.

输出:

```
I'm Intern At GeeksforGeeks.

```

**解释:**ucwords()函数将字符串中每个单词的第一个字母大写。它的原型如下:string ucwords(字符串字符串字符串)。