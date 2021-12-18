# PHP|ctype_lower()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_lower-function/](https://www.geeksforgeeks.org/php-ctype_lower-function/)

Ctype_lower()函数是 PHP 中的一个内置函数，用于检查字符串中给定的字符是否为小写。

**语法：**

```php
*bool* ctype_lower( *string* $text )
```

**参数：**此函数接受单个参数**$text**，该参数保存需要测试的字符串。

**返回值：**如果字符串的所有字符都是当前区域设置中的小写字符，则此函数返回 TRUE。

下面的程序演示了 PHP 中的 ctype_lower()函数：

**程序 1：**

```php
<?php 

// PHP program to check the string contains
// all lower case characters or not
$strings = array('gfg123', 'geeksforgeeks', 'GfG'); 

// Loop to check the above three strings
foreach ($strings as $testcase) { 
    if (ctype_lower($testcase)) { 
        echo "Yes\n"; 
    } else { 
        echo "No\n"; 
    } 
} 
?> 
```

**输出：**

```php
No
Yes
No

```

**程序 2：**

```php
<?php

// Declare a string
$str = "GeeksforGeeks"; 

$n = strlen($str); 

$count = 0;

for($i = 0; $i < $n; $i++) {
    if(ctype_lower($str[$i])) {
        $count++;
    }
}

echo "Totla number of lower case "
     . "character in string: "
     . $count;
?>
```

**输出：**

```php
Totla number of lower case character in string: 11

```

**引用：**[https://www.php.net/manual/en/function.ctype-lower.php](https://www.php.net/manual/en/function.ctype-lower.php)