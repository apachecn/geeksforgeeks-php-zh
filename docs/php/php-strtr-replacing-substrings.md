# PHP|strtr()，用于替换子字符串

> Original: [https://www.geeksforgeeks.org/php-strtr-replacing-substrings/](https://www.geeksforgeeks.org/php-strtr-replacing-substrings/)

它将一个字符串中的给定子字符串替换为另一个给定的字符串。 我们还可以使用它通过传递一组对来执行多个替换。

例如：

```php
Input : $str = "Hmrrb GmmksfbrGmmks";
        $from = "rbm";
        $to = "loe";
Output : Hello GeeksforGeeks

Input : $str = "Hello world";
        $arr = array("Hello" => "I Love", "world" => "GeeksforGeeks");
Output : I Love GeeksforGeeks

```

**语法：**

```php
string strtr ( string $string, string $from, string $to)

OR

string strtr (string $string, array $from_to_pairs)

```

**参数：**此函数接受三个/两个参数，所有参数都是必须传递的。
**字符串语法 1：**
**字符串：1.$String：**此参数表示给定的输入字符串。
**该参数表示要翻译的子字符串。2.$From：**此参数表示要翻译的子字符串。
**从 3.$到：**此参数表示“From”子串翻译后的子串。
**字符串语法 2：**
**字符串：1.$String：**此参数表示给定的输入字符串。
**从**到**对。$翻译 _ 对：**此参数表示包含各自的**从-到**对的数组。

**返回值：**此函数返回一个字符串，其中子字符串中**的所有字符都被给定字符串中的**到**子字符串替换。**

请注意，如果起始长度和终止长度不同，则输出将与最短的输出相关。
下面的程序说明了 PHP 中的 strtr()函数：

**程序 1：**

```php
<?php

// original string
$str = "GzzksworGzzks is zverything.";

// from and to terms
$from = "zw";
$to = "ef";

// calling strtr() function
$resStr = strtr($str, $from, $to);

print_r($resStr);

?>
```

发帖主题：Re：Kolibrios

```php
GeeksforGeeks is everything.

```

**程序 2：**

```php
<?php

// original string
$str = "Hi there";

// array declaring from-to pairs
$arr = array("Hi" => "Be", "there" => "Happy");

// calling strtr() function
$resStr = strtr($str, $arr);

print_r($resStr);

?>
```

发帖主题：Re：Kolibrios

```php
Be Happy

```

**引用：**[http://php.net/manual/en/function.strtr.php](http://php.net/manual/en/function.strtr.php)