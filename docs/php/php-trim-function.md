# PHP|trim()函数

> Original: [https://www.geeksforgeeks.org/php-trim-function/](https://www.geeksforgeeks.org/php-trim-function/)

PHP 中的**trim()**函数是一个内置函数，可以删除字符串左右两边的空格和预定义字符。

**相关函数**：

*   [PHP | ltrim () function](https://www.geeksforgeeks.org/php-ltrim-function/)
*   [PHP | rtrim () function](https://www.geeksforgeeks.org/php-rtrim-function/)

**语法：**

```
trim($string, $charlist)

```

**参数：**此函数接受一个必选参数和一个可选参数，如以上语法所示，如下所述。

1.  **$string** : this parameter specifies the string from which to remove spaces and left and right predefined characters
2.  **$charlist** : this is an optional parameter that specifies the characters to remove from the string. If this is not mentioned, all of the following characters are deleted:
    *   帖子主题：Re：Колибри
    *   "\ t"-Tab character
    *   "\ n"-newline character
    *   "\ x0B"-Vertical Tab
    *   "\ r"-enter
    *   ""-normal space

**返回值：**它通过删除字符串左右两侧的空格以及预定义字符来返回修改后的字符串。

以下程序说明了 Trim()函数：

**程序 1：**

```
<?php
// PHP program to demonstrate the use of trim() 
// function when second parameter is present

// removes the predefined characters from 
// front and back 
$str = "Hello World!";
echo trim($str, "Hell!");
?>
```

帖子主题：Re：Колибри

**程序 2：**

```
<?php
// PHP program to demonstrate the use of trim() 
// function when second parameter is absent

$str = "  geeks for geeks ";

// removes all leading and trailing whitespaces 
echo trim($str);
?>
```

帖子主题：Re：Колибри

**引用：**[http://php.net/manual/en/function.trim.php](http://php.net/manual/en/function.trim.php)