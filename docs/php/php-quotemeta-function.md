# PHP|Quotemeta()函数

> Original: [https://www.geeksforgeeks.org/php-quotemeta-function/](https://www.geeksforgeeks.org/php-quotemeta-function/)

**qutemeta()**函数是 PHP 中的一个内置函数，它接受一个字符串作为参数，并返回一个字符串，该字符串在字符串中的一些预定义字符前面添加了反斜杠。

预定义的字符包括：

*   句点(.)
*   反斜杠(\)
*   加号(+)
*   星号(*)
*   问号(？)
*   方括号([])
*   插入符号(^)
*   美元符号($)
*   括号(())

**语法：**

```php
 quotemeta($string)
```

**参数：**此函数只接受一个必选参数*$string*。 此参数指定要在上面提到的预定义字符前面添加反斜杠的字符串。

**返回值：**它通过在**$string**参数中的预定义字符前面添加反斜杠来返回字符串。

例如：

```php
Input:  $str = "geek$ for geeks?"
Output: geek\$ for geeks\?

Input: $str = "+geek* for geeks."
Output: \+geek\* for geeks\.

```

下面的程序演示了 PHP 中的 qutemeta()函数：

**程序 1：**当字符串有‘？’ 和‘{Content}#x2019；预定义字符

```php
<?php
// PHP program to demonstrate the 
// working of quotemeta() function 

$str = "geek$ for geeks?";

// prints the string by adding backslashes 
// in front of the predefined characters
// '{content}apos; and '?'
echo(quotemeta($str));
?>
```

产出：

```php
geek\$ for geeks\?
```

**程序 2：**当字符串有‘*’，‘.’ 和‘+’预定义字符

```php
<?php
// PHP program to demonstrate the 
// working of quotemeta() function 

$str = "+geek* for geeks.";

// prints the string by adding backslashes 
// in front of the predefined characters
echo(quotemeta($str));
?>
```

产出：

```php
\+geek\* for geeks\.
```

**程序 3：**当字符串以方括号和圆括号作为预定义字符时。

```php
<?php
// PHP program to demonstrate the 
// working of quotemeta() function 

$str = "[]geek for geeks()";

// prints the string by adding backslashes 
// in front of the predefined characters
// brackets and parenthesis
echo(quotemeta($str));
?>
```

产出：

```php
\[\]geek for geeks\(\)
```

**程序 4：**当字符串将脱字符(^)作为预定义字符时。

```php
<?php
// PHP program to demonstrate the 
// working of quotemeta() function 

$str = "2 ^ 2 = 4";

// prints the string by adding backslashes 
// in front of the predefined characters
// caret (^)
echo(quotemeta($str));
?>
```

产出：

```php
2 \^ 2 = 4
```

**引用：**
[http://php.net/manual/en/function.quotemeta.php](http://php.net/manual/en/function.quotemeta.php)