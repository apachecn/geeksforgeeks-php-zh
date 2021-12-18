# PHP|ctype_digit()(检查数值)

> Original: [https://www.geeksforgeeks.org/php-ctype_digit-function/](https://www.geeksforgeeks.org/php-ctype_digit-function/)

PHP 中的 ctype_digit()函数，用于检查文本的每个字符是否为数字。 如果字符串的所有字符都是数字，则返回 TRUE，否则返回 FALSE。

**语法：**

```php
ctype_digit(string text)

```

**使用的参数：**
PHP 中的 ctype_digit()函数只接受一个参数。

*   **text：**必选参数，指定测试字符串。

**返回值：**
如果字符串的所有字符都是数字，则返回 TRUE，否则返回 FALSE。

**错误和异常：**

1.  在传递字符串时给出预期结果，在传递整数时不给出期望的输出。
2.  对于 PHP 5.1.0 以前版本的空字符串，该函数返回 TRUE

例如：

```php
Input  :789495001
Output : Yes
Explanation : All digits, return True

Input  : 789.0877
Output : No
Explanation: String contains floating point, 
return false.                   

```

下面的程序说明了 ctype_digit()函数。

**程序：1**检查 ctype_digit()函数以查找包含所有数字的单个字符串。

```php
<?php
// PHP program to check given string is 
// control character

$string = '123456789';

    // Checking above given string 
    // by using of ctype_digit() function.
    if ( ctype_digit($string)) {

        // if true then return Yes
        echo "Yes\n";
    } else {

        // if False then return No
        echo "No\n";
    }

?>
```

**Output:**

```php
Yes

```

**程序：2**
驱动代码 ctype_digit()函数，其中输入将是包含特殊字符、整数、字符串的字符串数组。

```php
<?php
// PHP program to check is given string
// contains all digits using ctype_digit

$strings = array(
    'Geeks-2018',
    'geek@yahoo.com',
    '10.99999Fe',
    '12345',
    'geeksforgeeks.org'
);

// Checking above given strings 
//by used of ctype_digit() function .

foreach ($strings as $testcase) {

    if (ctype_digit($testcase)) {
        // if true then return Yes
        echo "Yes\n";
    } else {
        // if False then return No
        echo "No\n";
    }
}

?>
```

**Output:**

```php
No
No
No
Yes
No

```

**ctype_digit()vs is_int()**
ctype_digit()基本上用于字符串类型，is_int()用于整数类型。 Ctype_digit()遍历所有字符并检查每个字符是否都是数字。 例如,

```php
<?php
// PHP code to demonstrate difference between
// ctype_digit() and is_int().
$x = "-123";
if (ctype_digit($x))
   echo "Yes\n";
else 
   echo "No\n";

$x = -123;
if (is_int($x))
   echo "Yes";
else 
   echo "No";
?>
```

**Output:**

```php
No
Yes

```

加入时间：清华大学 2007 年 01 月 25 日下午 3：33