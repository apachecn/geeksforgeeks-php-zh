# PHP|字符串函数

> Original: [https://www.geeksforgeeks.org/php-string-functions/](https://www.geeksforgeeks.org/php-string-functions/)

我们已经在文章[PHP|String](https://www.geeksforgeeks.org/php-strings/)中了解了 PHP 中可用的一些基本字符串操作函数。 在本文中，我们将了解一些用于更改 PHP 中字符串大小写的字符串函数。 以下是 PHP 中一些最常用的字符串大小写操作函数：

PHP 中的**stroupper()函数**

此函数将字符串作为参数，并返回所有字符均为大写的字符串。

**语法**：

```php
strtoupper($string)
```

用于说明 stroupper()函数用法的程序：

```php
<?php
# PHP code to convert to Upper Case
function toUpper($string){
    return(strtoupper($string));
}

// Driver Code
$string="GeeksforGeeks";  
echo (toUpper($string));
?>  
```

产出：

```php
GEEKSFORGEEKS
```

PHP 中的**strtolower()函数**

此函数以字符串为参数，返回所有小写字符的字符串。

**语法**：

```php
strtolower($string)
```

演示 strtolower()函数用法的程序：

```php
<?php
# PHP code to convert to Lower Case
function toLower($string){
    return(strtolower($string));
}

// Driver Code
$string="GeeksforGeeks";  
echo (toLower($string));
?>  
```

产出：

```php
geeksforgeeks
```

**PHP**中的 ucfirst()函数

此函数将字符串作为参数，并返回第一个字符为大写的字符串，而字符的所有其他大小写保持不变。

**语法**：

```php
ucfirst($string)
```

说明 ucfirst()函数用法的程序：

```php
<?php
# PHP code to convert the first letter to Upper Case
function firstUpper($string){
    return(ucfirst($string));
}

// Driver Code
$string="welcome to GeeksforGeeks";  
echo (firstUpper($string));
?>
```

产出：

```php
Welcome to GeeksforGeeks
```

**PHP**中的 lcfirst()函数

此函数以字符串为参数，返回第一个字符为小写的字符串，其他所有字符保持不变。

**语法**：

```php
lcfirst($string)
```

演示 lcfirst()函数用法的程序：

```php
<?php
# PHP code to convert the first letter to Lower Case
function firstLower($string){
    return(lcfirst($string));
}

// Driver Code
$string="WELCOME to GeeksforGeeks";  
echo (firstLower($string));
?>
```

产出：

```php
wELCOME to GeeksforGeeks
```

**PHP**中的 ucwords()函数

此函数将字符串作为参数，并返回每个单词的第一个大写字符的字符串，其他所有字符保持不变。

**语法**：

```php
ucwords($string)
```

说明 ucword()函数用法的程序：

```php
<?php
# PHP code to convert the first letter 
# of each word to Upper Case
function firstUpper($string){
    return(ucwords($string));
}

// Driver Code
$string="welcome to GeeksforGeeks";  
echo (firstUpper($string));
?>
```

产出：

```php
Welcome To GeeksforGeeks
```

PHP 中的**strlen()函数**

此函数以字符串为参数，返回表示字符串长度的整数值。 它计算字符串的长度，包括所有空格和特殊字符。

**语法**：

```php
strlen($string)
```

演示 strlen()函数用法的程序：

```php
<?php
# PHP code to get the length of any string
function Length($string){
    return(strlen($string));
}

// Driver Code
$string="welcome to GeeksforGeeks";  
echo (Length($string));
?>
```

产出：

```php
24
```