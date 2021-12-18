# 使用 PHP

获取 URL 子域的程序

> Original: [https://www.geeksforgeeks.org/program-to-get-the-subdomain-of-a-url-using-php/](https://www.geeksforgeeks.org/program-to-get-the-subdomain-of-a-url-using-php/)

给定一个 URL，任务是从给定的 URL 获取子域。 使用 EXPLODE()函数将字符串拆分成数组，或者使用 preg_plit()函数通过正则表达式将给定的字符串拆分成数组。

**示例：**

```
Input : subdomain.example.com
Output : subdomain

Input : contribute.geeksforgeeks.org
Output : contribute

```

**方法 1：****[PHP|EXPLODE()](https://www.geeksforgeeks.org/php-explode-function/)函数：**EXPLODE()函数是 PHP 中的内置函数，用于将字符串拆分成不同的字符串。 函数的作用是：根据字符串分隔符拆分字符串，即在出现分隔符的地方拆分字符串。 此函数返回一个数组，其中包含通过拆分原始字符串形成的字符串。

**语法：**

```
*array* explode( separator, OriginalString, NoOfElements )
```

使用 EXPLODE()函数从 URL 获取子域。 使用 explode()函数获取子域比使用 preg_plit()函数获取子域更容易。

**示例 1：**

```
<?php

$URL = "subdomain.example.com";

// Split string into array
$arr = explode('.', $URL);

// Get the first element of array
$subdomain = $arr[0];

echo $subdomain;

?>
```

**Output:**

```
subdomain

```

**示例 2：**

```
<?php

$URL = "contribute.geeksforgeeks.org";

// Split string into array
$arr = explode('.', $URL);

// Get the first element of array
$subdomain = $arr[0];
echo $subdomain;

?>
```

**Output:**

```
contribute

```

**方法 2：****[PHP|preg_plit()](https://www.geeksforgeeks.org/php-preg_split-function/)函数：**preg_plit()函数是 PHP 中的一个内置函数，用于通过正则表达式将给定的字符串转换为数组。 如果匹配失败，将返回一个包含输入字符串的单个元素的数组。

**语法：**

```
*array* preg_split( $pattern, $subject, $limit, $flag )
```

使用 preg_plit()函数从 URL 获取子域。 将正则表达式作为参数传递给函数并拆分 URL。

**示例 1：**

```
<?php

$URL = "contribute.geeksforgeeks.org";

// Escape '.' as special symbol for regular expression.
$arr = preg_split('[\.]', $URL); 

$subdomain = $arr[0];

echo $subdomain;
?>
```

**Output:**

```
contribute

```

**示例 2：**

```
<?php

$URL = "ide.geeksforgeeks.org";

// Escape '.' as special symbol for regular expression.
$arr = preg_split('[\.]', $URL); 

$subdomain = $arr[0];

echo $subdomain;

?>
```

**Output:**

```
ide

```