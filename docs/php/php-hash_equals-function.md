# PHP|hash_equals()函数

> Original: [https://www.geeksforgeeks.org/php-hash_equals-function/](https://www.geeksforgeeks.org/php-hash_equals-function/)

Hash_equals 函数()是 PHP 中的一个内置函数，用于使用相同的时间比较两个字符串，无论它们是否相等。
**语法：**和

```php
hash_equals( $known_str, $usr_str )
```

**参数：**此函数接受上述两个参数，如下所述。

*   **$KNOWN_STR：**此参数用于指定已知长度字符串。
*   **$usr_str：**此参数用于指定用户提供的字符串。

**返回值：**如果两个字符串相等，则此函数返回 True，否则返回 False。
下面的程序说明了 PHP 中的 hash_equals()函数：
**程序 1：**和

## PHP

```php
<?php

// PHP program to illustrate
// hash_equals function
$known_str = crypt('GFG', 'Hello-GFG');
$usr_str   = crypt('GFG', 'Hello-GFG');

// Compare both strings
$res = hash_equals($known_str, $usr_str);

// Display result
var_dump($res);
?>
```

**Output:** 

```php
bool(true)
```

**程序 2：**和

## PHP

```php
<?php

// PHP program to illustrate
// hash_equals function
$known_str = crypt('GFG', 'Hello-GFG');
$usr_str   = crypt('GeeksforGeeks', 'Hello-GFG');

// Compare both strings
$res = hash_equals($known_str, $usr_str);

// Display result
var_dump($res);
?>
```

**Output:** 

```php
bool(false)
```

**引用：**[http://php.net/manual/en/function.hash-equals.php](http://php.net/manual/en/function.hash-equals.php)