# PHP|str_iplace()函数

> Original: [https://www.geeksforgeeks.org/php-str_ireplace-function/](https://www.geeksforgeeks.org/php-str_ireplace-function/)

Str_iplace()是 PHP 中的一个内置函数，用于将搜索字符串或搜索字符串数组中出现的所有内容分别替换为给定字符串或数组中的替换字符串或替换字符串数组。 此函数以不区分大小写的方式执行搜索。 此函数类似于[str_place()](https://www.geeksforgeeks.org/php-str_replace-function/)函数。 不同之处在于 str_place()函数区分大小写，而 str_iplace()不区分大小写。

**语法：**

```
str_ireplace ( $searchVal, $replaceVal, $subjectVal, $count )
```

**参数**：该函数接受 4 个参数，其中 3 个是必选的，1 个是可选的。 所有这些参数如下所述：

1.  **$searchVal**：此参数可以是字符串类型，也可以是数组类型。 此参数指定要搜索和替换的字符串。
2.  **$replaceVal**：此参数可以是字符串类型，也可以是数组类型。 此参数指定要用来替换$searchVal 字符串的字符串。
3.  **$subjectVal**：此参数可以是字符串类型，也可以是数组类型。 此参数指定要搜索$searchVal 并替换为$replaceVal 的字符串或字符串数组。
4.  **$count**：该参数是可选的，如果传递，它的值将被设置为对字符串$subjectVal 执行的替换操作的总数。

如果**$searchVal**和**$replaceVal**参数是数组，则在$subjectVal 字符串中搜索$searchVal 参数的所有元素，并替换为$replaceVal 参数中的相应元素。 如果$replaceVal 中的元素数少于$searchVal 数组中的元素数，则如果$subjectVal 参数中出现$searchVal 参数的附加元素，则它们将被空字符串替换。 如果$subjectVal 参数也是数组而不是字符串，则将搜索$subjectVal 的所有元素。

**返回值**：此函数返回一个字符串或基于$subjectVal 参数的数组，其中包含替换的值。

例如：

```
Input : $subjectVal = "How ARE you", $searcVal = "are"
        $replaceVal = "is"
        str_ireplace($searchVal,$replaceVal,$subjectVal);
Output : How is you 

Input : $subjectVal = "Geeks are Geeks", $searcVal = "are"
        $replaceVal = "for"
        str_ireplace($searchVal,$replaceVal,$subjectVal);
Output : Geeks for Geeks

```

下面的程序演示了 PHP 中的 str_iplace()函数：

**程序 1：**此程序显示 str_iplace()函数不区分大小写。

```
<?php

// Input string
$subjectVal="how are you";

// using str_ireplace() function
$res = str_ireplace("are", "is", $subjectVal);

echo $res;

?>

```

产出：

```
how is you
```

**程序 2：**

```
<?php

// Input string
$subjectVal="Geeks are Geeks";

// using str_ireplace() function
$res = str_ireplace("are", "for", $subjectVal);

echo $res;

?>

```

产出：

```
Geeks for Geeks
```

**引用：**
[http://php.net/manual/en/function.str-ireplace.php](http://php.net/manual/en/function.str-ireplace.php)