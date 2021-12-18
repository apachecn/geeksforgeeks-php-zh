# 如何在 PHP 中删除字符串中所有不可打印的字符？

> 原文:[https://www . geesforgeks . org/如何删除所有不可打印的 php 字符串字符/](https://www.geeksforgeeks.org/how-to-remove-all-non-printable-characters-in-a-string-in-php/)

给定一个包含可打印和不可打印字符的字符串。任务是从字符串中删除所有不可打印的字符。Space()是第一个可打印的字符，tilde (~)是最后一个可打印的 ASCII 字符。因此，任务是替换所有落在该范围内的字符，这意味着只取那些出现在范围(32-127)内的字符。这个任务只由不同类型的正则表达式完成。

**示例:**

```
Input: str = "\n\nGeeks \n\n\n\tfor Geeks\n\t"
Output: Geeks for Geeks

```

**注意:**换行符(\n)和制表符(\t)是不可打印字符的命令。

**方法 1:使用通用正则表达式:**有很多正则表达式可用。最好的解决方案是从输入字符串中去除所有非 ASCII 字符，这可以通过 preg_replace 来完成。

**示例:**

```
<?PHP
// PHP program to remove all non-printable
// character from string

// String with non printable characters
$str = "Geeks šžfor ÂGee\tks\n";

// Using preg_replace method to remove all 
// non-printable character from string
$str = preg_replace('/[\x00-\x1F\x80-\xFF]/', '', $str);

// Display the modify string
echo($str);

?>
```

**Output:**

```
Geeks for Geeks

```

**方法 2:使用‘print’正则表达式:**其他可能的解决方案是使用 **print** 正则表达式。**【:print:】**正则表达式代表**“任意可打印字符”**。

**示例:**

```

<?PHP
// PHP program to remove all non-printable
// character from string

// String with non printable char
$str = "Geeks šžfor ÂGee\tks\n";

// Using preg_replace method to remove all 
// non-printable character from string
$str = preg_replace('/[[:^print:]]/', '', $str);

// Display modify string
echo($str);

?>
```

**Output:**

```
Geeks for Geeks

```