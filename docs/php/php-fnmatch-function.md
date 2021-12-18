# PHP|fnMatch()函数

> Original: [https://www.geeksforgeeks.org/php-fnmatch-function/](https://www.geeksforgeeks.org/php-fnmatch-function/)

PHP 中的 fnMatch()函数用于将文件名或字符串与指定模式进行匹配。 要检查的模式和文件名作为参数发送给 fnMatch()函数，如果找到匹配则返回 True，如果失败则返回 False。
fnMatch()函数现在可用于 PHP 5.3.0 版本上的 Windows 平台。

**语法：**

```php
fnmatch(pattern, string, flags)
```

**使用的参数：**
PHP 中的 fnMatch()函数接受三个参数。

1.  **模式：**指定要搜索的模式的强制参数。
2.  **字符串：**必选参数，指定要检查的字符串或文件。
3.  **标志：**可选参数，用于指定标志或标志组合。
    标志可以是以下标志的组合：
    *   FNM_PATHNAME：它用于指定字符串中的斜杠只与给定模式中的斜杠匹配。
    *   FNM_NOESCAPE：用于禁用反斜杠转义。
    *   FNM_CASEFOLD：用于无大小写匹配。
    *   FNM_PERIOD：用于指定字符串中的前导句点必须与给定模式中的句点完全匹配。

**返回值：**
如果找到匹配项，则返回 True，如果失败，则返回 False。

**错误和异常：**

1.  如果多次使用 fnMatch()函数，则必须清除缓冲区。
2.  FnMatch()函数返回布尔值 False，但很多时候它返回的是非布尔值，计算结果为 False。

下面的程序演示了 fnMatch()函数。

**程序 1**假设有一个名为“gfg.txt”的文件

```php
<?php
$check = "gfg.txt";

// fnmatch function used to check
 for file starting with g
if (fnmatch("*[g]*",$check))
{
   echo "gfg";
}
else
{
   echo "match not found";
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg
```

**程序 2**

```php
<?php

$check = "GeeksforGeeks";

// fnmatch function used to check for 
// a word practice or practise
if (fnmatch("*Geeks[gfgj]orGeeks", $check))
    echo "Yes";
else
    echo "No";
?>
```

**Output:**

```php
Yes

```

**程序 3**

```php
<?php
$check = 'GFG A computer science portal';

// fnmatch function used to check 
// for a word php without considering its case 
if (fnmatch("*[PUTgfg]*", $check, FNM_CASEFOLD))
    echo "Yes";
else
    echo "No";

?>
```

**Output:**

```php
Yes

```

**程序 4**

```php
<?php

$check = "There is a back slash \ in this sentence";

// fnmatch function used to check for a \ 
if (fnmatch("*[\]*", $check, FNM_NOESCAPE))
    echo "back slash  (\)  in the sentence ";
 else
    echo "match not found";
?>
```

**Output:**

```php
back slash  (\)  in the sentence

```

**引用：**
[http://php.net/manual/en/function.fnmatch.php](http://php.net/manual/en/function.fnmatch.php)