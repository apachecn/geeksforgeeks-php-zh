# PHP|ctype_xdigit()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_xdigit-function/](https://www.geeksforgeeks.org/php-ctype_xdigit-function/)

PHP 中的**ctype_xdigit()**函数用于检查字符串/文本的每个字符是否为十六进制数字。 如果所有字符都是十六进制，则返回**TRUE**，否则返回**FALSE**。

**语法：**

```php
*ctype_xdigit(string text)*

```

**使用的参数：**

*   **text：**必选参数，指定测试字符串。

**返回值：**
如果字符串的所有字符都是十六进制，则返回 TRUE，否则返回 FALSE。

**示例：**

```php
Input  :  ABCDEF0123
Output :  Yes

Input  : GFG2018
Output : No

```

```php
Note :  It checking decimal digit or a character from [A-F, a-f].
```

下面的程序说明了 ctype_xdigit()函数。

**程序：1**

```php
<?php
// PHP program to check given string is 
// Hexadecimal character or not

$string = 'ABab012';

// Checking above string by using
// of ctype_xdigit() function.
if ( ctype_xdigit($string)) {

    // if true then return Yes
    echo "Yes \n";

} else {

    // if False then return No
    echo "No \n";
}
?>
```

**Output:**

```php
Yes

```

**程序：2**
再举一个例子**ctype_xdigit()**函数，通过将输入作为字符串数组，检查当输入包含大写、小写和符号字符时，它是如何工作的。

```php
<?php
// PHP program to check given string is 
//Hexadecimal character or not

$strings = array(
    'ABCDEF',
    'abcdef',
    '0123456789X',
    '0123456789',
    'Gg@(*&)',
    'GFG'
);

// Checking above given strings 
//by used of ctype_xdigit() function .
foreach ($strings as $test) {

    if (ctype_xdigit($test)) {
         echo "Yes \n";
    } else {
         echo "No \n";
    }
}

?>
```

**Output:**

```php
Yes 
Yes 
No 
Yes 
No 
No

```

**引用：**[http://php.net/manual/en/function.ctype-xdigit.php](http://php.net/manual/en/function.ctype-xdigit.php)