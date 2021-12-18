# PHP|urlencode()函数

> Original: [https://www.geeksforgeeks.org/php-urlencode-function/](https://www.geeksforgeeks.org/php-urlencode-function/)

Urlencode()函数是 PHP 中的一个内置函数，用于对 url 进行编码。 此函数返回一个字符串，该字符串包含除-_ 之外的所有非字母数字字符。 并替换为百分号(%)，后跟两个十六进制数字和编码为加号(+)的空格。

**语法：**

```php
*string* urlencode( $input )
```

**参数：**此函数接受单个参数*$input*，该参数用于保存要编码的 url。

**返回值：**此函数在成功时返回编码字符串。

下面的程序演示了 PHP 中的 urlencode()函数：

**程序 1：**

```php
<?php

// PHP program to illustrate urlencode function
echo urlencode("https://geeksforgeeks.org/") . "\n";

?>
```

**输出：**

```php
https%3A%2F%2Fgeeksforgeeks.org%2F

```

**程序 2：**

```php
<?php

// PHP program to illustrate urlencode function
echo urlencode("https://ide.geeksforgeeks.org/") . "\n";
echo urlencode("https://write.geeksforgeeks.org/") . "\n";
echo urlencode("https://practice.geeksforgeeks.org/") . "\n";
echo urlencode("https://geeksforgeeks.org/") . "\n";

?>
```

**输出：**

```php
https%3A%2F%2Fide.geeksforgeeks.org%2F
https%3A%2F%2Fwrite.geeksforgeeks.org%2F
https%3A%2F%2Fpractice.geeksforgeeks.org%2F
https%3A%2F%2Fgeeksforgeeks.org%2F

```

**引用：**[http://php.net/manual/en/function.urlencode.php](http://php.net/manual/en/function.urlencode.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。