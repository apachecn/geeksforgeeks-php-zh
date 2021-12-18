# PHP|strcasecmp()函数

> Original: [https://www.geeksforgeeks.org/php-strcasecmp-function/](https://www.geeksforgeeks.org/php-strcasecmp-function/)

**strcasecmp()**函数是 PHP 中的内置函数，用于比较两个给定的字符串。 它不区分大小写。 此函数类似于 strncasecmp()，唯一的区别是 strncasecmp()提供了指定每个字符串中用于比较的字符数的规定。

**语法：**

```php
strcasecmp($string1, $string2)
```

**参数：**此函数接受上述语法中所示的两个必选参数，如下所示：

**$STRIN1，$STRIN2：**这些参数指定要比较的字符串。

**返回值：**
此函数根据以下条件返回一个整数：

*   Strcasecmp()返回 0-如果两个字符串相等。
*   Strcasecmp()返回<0-如果字符串 1 小于字符串 2
*   Strcasecmp()返回>0-如果字符串 1 大于字符串 2

**示例：**

```php
Input : $str1 = "Geeks for Geeks "
        $str2 = "Geeks for Geeks "
Output : 0

Input : $str1 = "Geeks for Geeks"
        $str2 = "Hello Geek!"
Output : -1

```

下面的程序演示了 PHP 中的**strcasecmp()**函数：

**程序 1：**当两个字符串相同时：

```php
<?php
// PHP program to demonstrate the use
// of strcasecmp() function

$str1 = "Geeks for Geeks ";
$str2 = "Geeks for Geeks ";

// Both the strings are equal
$test=strcasecmp($str1, $str2); 

echo "$test"; 

?>
```

产出：

```php
0
```

**程序 2：**当两个字符串不相同时：

```php
<?php
// PHP program to demonstrate the use
// of strcasecmp() function

$str1 = "Geeks for Geeks";
$str2 = "Hello Geek!";

// Both the strings are not equal
//  str1 < str2 

$test = strcasecmp($str1, $str2); 

echo "$test"; 

?>
```

产出：

```php
-1
```

**程序 3：**当两个字符串不相同时：

```php
<?php
// PHP program to demonstrate the use
// of strcasecmp() function
$str1 = "Hello Geek!";
$str2 = "Geeks for Geeks";

// Both the strings are not equal
//  str1 > str2 
$test = strcasecmp($str1, $str2); 

echo "$test"; 

?>
```

产出：

```php
1
```

**参考**：
[http://php.net/manual/en/function.strcasecmp.php](http://php.net/manual/en/function.strcasecmp.php)