# 如何在 PHP 中使用 preg_replace()函数从文件中删除文本？

> 原文:[https://www . geesforgeks . org/如何使用-preg_replace-function-in-php 从文件中删除文本/](https://www.geeksforgeeks.org/how-to-delete-text-from-file-using-preg_replace-function-in-php/)

给定一个包含一些元素的文件，任务是使用 [preg_replace()函数](https://www.geeksforgeeks.org/php-preg_replace-function/)删除文件的内容。preg_replace()函数搜索文件中的字符串模式，如果找到字符串模式，则用所需的字符串进行替换。简单地说，它可以修改文件的内容。

**语法:**

```
preg_replace( $pattern,  $replacement, $subject);
```

**参数:**

*   **$pattern:** 包含我们要替换的字符串。
*   **$replacement:** 它包含将替换现有字符串的字符串。
*   **$subject:** 它包含需要移除字符串的主字符串文件。

我们创建了一个名为**水果. txt**
**水果. txt** 的文本文件

```
mango
apple
papaya
guava
apple
grapes
mango
apple
```

**程序 1:** 该程序从给定文件中删除所有字符串。

```
<?php

$a = 'fruits.txt';
$b = file_get_contents('fruits.txt');
echo "File contents before using "
        . "preg_replace() function<br>";
echo $b;
echo "<br><br>File contents after using "
        . "preg_replace() function<br> ";
$c = preg_replace('/[a-z]/', '', $b);
echo $c;
file_put_contents($a, $c);
?>
```

**输出:**

```
File contents before using preg_replace() function
mango apple papaya guava apple grapes mango apple

File contents after using preg_replace() function
```

**程序 2:** 该程序使用 preg_replace()函数从文件中删除特定内容。

```
<?php

$a = 'fruits.txt';

$b = file_get_contents('fruits.txt');

echo "File contents before using "
        + "preg_replace() function<br>";
echo $b;

echo "<br><br>File contents after using "
        + "preg_replace() function<br>";

$c = preg_replace('/[a]/', '', $b);
echo $c;

file_put_contents($a, $c); 
?>
```

**输出:**

```
File contents before using preg_replace() function
mango apple papaya guava apple grapes mango apple

File contents after using preg_replace() function
mngo pple ppy guv pple grpes mngo pple
```

**程序 3:** 该程序从文件中删除整个单词。

```
<?php

$a = 'fruits.txt';

$b = file_get_contents('fruits.txt');

echo "File contents before using "
        . "preg_replace() function<br>";
echo $b;

echo "<br><br>File contents after using "
        . "preg_replace() function<br>";

$c = preg_replace('/apple/', '', $b);
echo $c;

file_put_contents($a, $c); 
?>
```

**输出:**

```
File contents before using preg_replace() function
mango apple papaya guava apple grapes mango apple

File contents after using preg_replace() function
mango papaya guava grapes mango
```