# PHP|ctype_space()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_space-function/](https://www.geeksforgeeks.org/php-ctype_space-function/)

PHP 中的 ctype_space()函数用于检查字符串的每个字符是否为空格字符。 如果所有字符都是空格，则返回 True，否则返回 False。

**语法：**

```php
*ctype_space(string text)*

```

**使用的参数：**

*   **文本：-**指定字符串的必选参数。

**返回值：**
如果文本中的每个字符都包含空格，则返回 TRUE，否则返回 FALSE。 空白字符也包括制表符、回车符、垂直制表符、换行符和换页符。

**示例：**

```php
Input  : \r   
Output : Yes
Explanation: \r is create white space

Input  : abc\r
Output : No   
Explanation: characters "abc" are not white space

```

下面的程序演示了 ctype_space()函数。
**程序 1：**接受单个字符串

```php
<?php
// PHP program to check given string is 
// whitespace character or not

$string = "/n/t/r";

if (ctype_space($string)) 
   echo "Yes \n";
else 
   echo "No \n";   
?>
```

**Output:**

```php
No

```

**程序：2**获取字符串数组并使用 ctype_space()函数检查空格

```php
<?php
// PHP program to check given string is 
// whitespace  character or not

$strings = array('\n\y\t\x\u\o', "\ngfg\n", "\t");

// Checking above given strings 
//by used of ctype_space()function .
foreach ($strings as $testcase) {

    if (ctype_space($testcase)) {
        echo "Yes \n";
    } else {
        echo "No \n";
    }
}
?>
```

**Output:**

```php
No 
No 
Yes

```

**程序：3**
以**ctype_space()**函数为例，说明如何使用单引号‘’和双引号“”符号处理字符串。

```php
<?php
// PHP program to check given string is 
// whitespace  character or not

$strings = array('\n', "\n", '\t', "\t");

// Checking above given strings 
// by used of ctype_space()function .

foreach ($strings as $testcase) {

    if (ctype_space($testcase)) {
        echo "Yes \n";
    } else {
        echo "No \n";
    }
}
?>
```

**Output:**

```php
No 
Yes 
No 
Yes

```

**引用：**[http://php.net/manual/en/function.ctype-space.php](http://php.net/manual/en/function.ctype-space.php)