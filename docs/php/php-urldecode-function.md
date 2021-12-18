# PHP|urldecode()函数

> Original: [https://www.geeksforgeeks.org/php-urldecode-function/](https://www.geeksforgeeks.org/php-urldecode-function/)

Urldecode()函数是 PHP 中的内置函数，用于解码由 encode()函数编码的 url。
**语法：**

```php
*string* urldecode( $input )
```

**参数：**此函数接受保存要解码的 url 的单个参数*$input*。

**返回值：**此函数在成功时返回解码后的字符串。

下面的程序说明了 PHP 中的 urldecode()函数：
**程序 1：**

```php
<?php

// PHP program to illustrate urldecode function

// all sub domain  of geeksforgeeks
echo urldecode("https%3A%2F%2Fide.geeksforgeeks.org%2F"). "\n";
echo urldecode("https%3A%2F%2Fpractice.geeksforgeeks.org%2F"). "\n";
echo urldecode("https%3A%2F%2Fgeeksforgeeks.org%2F"). "\n";
?>
```

**Output:**

```php
https://ide.geeksforgeeks.org/
https://practice.geeksforgeeks.org/
https://geeksforgeeks.org/

```